# Passwordless Authentication In Ansible

Passwordless authentication simplifies connecting to remote machines and running tasks automatically without needing to enter a password. You do this by creating an SSH key pair on your Ansible control node and copying the public key to the target machine’s authorized_keys file.

<img width="957" height="410" alt="image" src="https://github.com/user-attachments/assets/2fae9e20-3cda-4d3c-877b-451e2989c1bc" />


### Steps to Set Up SSH Key-based Authentication:

1. #### Generate SSH Key Pair on Ansible Control Node: 
Run the following command to generate an SSH key pair:

```
ssh-keygen
```
<img width="899" height="296" alt="image" src="https://github.com/user-attachments/assets/d44b11ef-51a8-48a0-acb5-1d25ce787f61" />

The command generates a public and private key pair in your .ssh directory.

2. #### Distribute Public Key: 
Copy the public key from the Ansible control node to the authorized_keys file of the user on each managed node that Ansible will connect to.

```
ssh-copy-id ubuntu@IPADDRESS
```
This command securely copies the public key and sets the correct permissions.

3. #### Verify Passwordless Login: 
Test passwordless authentication by trying to SSH into the target machine:

```
ssh ubuntu@IPADDRESS
```
<img width="939" height="407" alt="image" src="https://github.com/user-attachments/assets/757ce33e-9c45-48c4-9b5d-a6d0b28a5439" />
