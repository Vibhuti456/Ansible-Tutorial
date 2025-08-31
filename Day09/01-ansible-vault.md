
### Ansible Vault

Storing secrets securely is crucial, and Ansible Vault provides a secure way to manage sensitive information such as passwords, API keys, or any other confidential data within your Ansible playbooks or files. Ansible Vault encrypts these sensitive values so that they are stored in an encrypted format and can only be decrypted with the correct password or secret key.

Here’s a step-by-step guide on how to use Ansible Vault to store secrets:

#### Creating an Encrypted File with Ansible Vault:

1. #### Create a New Encrypted File:
Use the ansible-vault create command to create a new encrypted file. For example:

```
ansible-vault create secret_vars.yml
```
This command will prompt you to enter and confirm a password for the new vault file.

#### 2. Add Secrets to the Encrypted File:
The file will open in your default text editor. Add your secrets in the YAML format, for instance:

```
database_password: your_secure_password
api_key: your_api_key
other_secret: sensitive_information
```
Save and close the file. It will now be encrypted with the password you provided.

#### Editing an Existing Encrypted File:
To edit an existing encrypted file, use the ansible-vault edit command:

```
ansible-vault edit secret_vars.yml
```

This command will prompt you to enter the password to unlock and edit the file.
