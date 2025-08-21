
### Output of all the tasks

#### Task 1 - Solution

1. Create an IAM user in AWS to provisioning the AWS ec2 instances.

2. Once created the access key run the below to create a vault in your control node (localhost).

```
openssl rand -base64 2048 > vault.pass
```
```
ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass
```

Then enter your access key and secret key inside the file and save it. 

#### Note: Use the same value pair inside the vault file which used in playbook or in task. 

```
aws_access_key: "{{ec2_access_key}}"  
aws_secret_key: "{{ec2_secret_key}}"  
```
```
ec2_access_key: ACCESS KEY 
ec2_secret_key: SECRET KEY
```

3. Run the ansible playbook command: 
```
ansible-playbook -i inventory.ini ec2_create.yml --vault-password-file vault.pass
```

#### Output shows like: 
<img width="959" height="233" alt="image" src="https://github.com/user-attachments/assets/27f6a171-079b-4780-97a8-61f4028c71e2" />
<img width="798" height="161" alt="instances" src="https://github.com/user-attachments/assets/ede1cd81-c760-4b59-93e9-4447e096e152" />

#### Task 1 has completed!!!!

#### Task 2 - Solution 

#### Passwordless Authentication 

1. Once all instances are running state add SSH inbound rules and do ssh-keygen on managed nodes.
```
ssh-keygen
```
2. After doing ssh-keygen add public of control node in the managed nodes.
3. Now try to do ssh to your managed nodes from the control node.
#### Amazon Linux SSH -    
<img width="555" height="175" alt="image" src="https://github.com/user-attachments/assets/a16b4d2e-854c-43dc-8744-71bcfbbe52a9" />
#### Ubuntu Linux SSH - 
<img width="925" height="454" alt="image" src="https://github.com/user-attachments/assets/5427af29-0e11-4669-869f-9bce6b2a9119" />
#### Ubuntu Linux SSH -
<img width="908" height="467" alt="image" src="https://github.com/user-attachments/assets/daeccf4d-94a7-4a4f-8bd5-741e7c6f3148" />

#### Task2 has completed!!!!

#### Task 3 - Solution 

#### Shutting down 2 ubuntu EC2 instances only 

1. Run below command and run the ansible playbook to shut down two EC2 machines.
```
ansible-playbook -i inventory.ini ec2-stop.yml --vault-password-file vault.pass
```
<img width="946" height="434" alt="image" src="https://github.com/user-attachments/assets/d3fda052-bf03-4914-b42f-582912268011" />

<img width="766" height="205" alt="stop" src="https://github.com/user-attachments/assets/5f24859e-9a00-441a-b14c-1c1cb2256d2b" />

#### Task3 has completed!!!!!

