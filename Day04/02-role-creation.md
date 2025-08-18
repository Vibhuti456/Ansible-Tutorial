### Roles creation and execution 

To create a role for your ansible automation tasks run the following command:

```
ansible-galaxy role init httpd
```
<img width="857" height="118" alt="image" src="https://github.com/user-attachments/assets/f80735b9-d3e4-4bdf-9a43-f9e634f401dc" />

role folder httpd has been created and has number of files inside it.

<img width="859" height="253" alt="image" src="https://github.com/user-attachments/assets/021b4243-b20b-4fad-9ca0-6b8c80d63186" />

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


