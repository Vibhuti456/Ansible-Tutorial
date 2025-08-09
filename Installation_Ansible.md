
# Installation Of Ansible

Ansible can be installed on Ubuntu using the system's package manager, apt, either from the default Ubuntu repositories or from the official Ansible PPA (Personal Package Archive).

Installation using the Ansible PPA (Recommended for latest versions):

### Update system packages

```
sudo apt update
```
<img width="623" height="332" alt="image" src="https://github.com/user-attachments/assets/d6d6eae5-3547-4bbf-9775-2579670a6d5e" />

1. Install software-properties-common: This package provides the add-apt-repository command.

```
sudo apt install software-properties-common -y
```
<img width="578" height="152" alt="image" src="https://github.com/user-attachments/assets/f8e18926-7fc8-4995-8c28-34d23520df73" />

2. Add the Ansible PPA.

```
sudo add-apt-repository --yes --update ppa:ansible/ansible
```
<img width="944" height="428" alt="image" src="https://github.com/user-attachments/assets/32a2c909-3639-444a-b052-7927f1d39b03" />

3. Install Ansible.

```
sudo apt install ansible -y
```
<img width="949" height="254" alt="image" src="https://github.com/user-attachments/assets/277c9da1-e28c-4c87-af7c-b5e09383497a" />

4. Verification:
After installation, verify that Ansible is installed and check its version: 

```
ansible --version
``` 
<img width="866" height="200" alt="image" src="https://github.com/user-attachments/assets/2bfe170a-e3e6-4323-bb1a-78e33f89f8f4" />
