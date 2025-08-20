#### Prerequisites of using Ansible collections

1. #### Installation of python-pip:
```
 sudo apt install python3-pip
 ```
<img width="952" height="380" alt="image" src="https://github.com/user-attachments/assets/9b249a9c-b8da-4465-94d4-5fd84b3dfdfa" />

2. #### Install Boto3:
```
pip install boto3
```
<img width="943" height="437" alt="image" src="https://github.com/user-attachments/assets/b38d0ef8-f945-4776-9acd-945d55e14ad9" />

3. #### Install AWS Collection:
```
ansible-galaxy collection install amazon.aws
```
<img width="949" height="68" alt="image" src="https://github.com/user-attachments/assets/f181ea06-34b1-496a-a63c-e1101c78aa83" />

### Setup Vault
1. Create a password for vault
```
openssl rand -base64 2048 > vault.pass
```

2. Add your AWS credentials using the below vault command
```
ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass
```

3. Now run your playbook with following command
```
ansible-playbook -i inventory.ini ec2-create.yml --vault-password-file vault.pass
```
<img width="943" height="262" alt="image" src="https://github.com/user-attachments/assets/e9f8f7a7-504b-4777-89b7-66b4d2ab6ed4" />

Creaated EC2 instance with Ansible modules on AWS

<img width="765" height="109" alt="image" src="https://github.com/user-attachments/assets/c723235b-c482-40c5-806d-ef0454ac42bd" />



