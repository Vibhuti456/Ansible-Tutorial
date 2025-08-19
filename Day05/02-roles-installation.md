### Role Installation from Ansible Galaxy

Ansible-Galaxy, on the other hand, is a hub used to share Ansible roles. Ansible-Galaxy can be used to install roles.

1. To install a role, you would have to run the following :

```
ansible-galaxy role install username.rolename
```

2. You can also create your own role by typing the following command:

```
ansible-galaxy role init rolename 
```

3. Here is a view of the Ansible Galaxy website:

<img width="957" height="436" alt="image" src="https://github.com/user-attachments/assets/f25633d2-308c-4c86-9e86-062e4376cd99" />

To install this, I would have to run:

```
ansible-galaxy role install rupeshsingh781.dockerinstallrole
```
#### Demo: 

1. Installation:
<img width="944" height="388" alt="image" src="https://github.com/user-attachments/assets/98606eca-27ba-45a5-bd92-e0a93e5ab369" />

2. Location of role:
<img width="953" height="379" alt="image" src="https://github.com/user-attachments/assets/67a7c005-4823-477a-b09e-4d1b9bf4dd97" />

3. Screenprint of Installation of Docker on managed node:
<img width="959" height="340" alt="image" src="https://github.com/user-attachments/assets/a00577ee-bc4c-46f6-82df-c7d2e2003d9d" />

<img width="955" height="326" alt="image" src="https://github.com/user-attachments/assets/4950ebb7-5413-4eaf-ad3a-5eeb3cc724a9" />

4. Managed Node Screenprint to check Docker Installation:

<img width="959" height="350" alt="image" src="https://github.com/user-attachments/assets/a80b8d45-9670-4f50-9c17-43a2a18040d6" />

#### Docker has been installed through Ansible Roles!!!!
