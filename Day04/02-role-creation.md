### Roles creation and execution 

To create a role for your ansible automation tasks run the following command:

```
ansible-galaxy role init httpd
```
<img width="857" height="118" alt="image" src="https://github.com/user-attachments/assets/f80735b9-d3e4-4bdf-9a43-f9e634f401dc" />

Role folder httpd has been created and has number of files inside it.

<img width="852" height="104" alt="image" src="https://github.com/user-attachments/assets/95979bcf-4388-4b47-a45b-5a7b65db89aa" />

<img width="860" height="199" alt="image" src="https://github.com/user-attachments/assets/ec04e143-498d-455c-821f-00bb57a3bd07" />

Now, using the previous ansible playbook we created a role and define each plays, tasks inside the role httpd that we created.
```
<role_name>/
  ├── defaults/
  │   └── main.yml
  ├── files/
  ├── handlers/
  │   └── main.yml
  ├── meta/
  │   └── main.yml
  ├── tasks/
  │   └── main.yml
  ├── templates/
  ├── vars/
      └── main.yml
```

For checking roles are working fine, we ran ansible-playbook.yml and located the index.html file inside the files folder and ran following command:

```
ansible-playbook -i inventory.ini first_playbook.yml
```
<img width="953" height="290" alt="image" src="https://github.com/user-attachments/assets/54572e08-9f0e-4c4c-be8d-984e5c62f1f8" />

In image we can see that it has changed one task and execute the action wrritten in ansible-playbook in managed node. 


