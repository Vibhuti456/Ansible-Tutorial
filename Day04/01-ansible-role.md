### Ansible Roles

Ansible roles are a way to structure and organize Ansible code, promoting reusability and maintainability. They encapsulate tasks, variables, handlers, and other related files into a standardized directory structure, making it easier to manage complex automation tasks and share them across projects. Roles are not executable on their own but are designed to be included and used within playbooks. 

### Why Ansible Roles? 


1. #### Modularity: 
Roles break down complex automation into smaller, manageable components, improving code organization and readability. 

2. #### Reusability:
Roles can be easily reused across different projects, reducing code duplication and saving time. 

3. #### Maintainability:
The standardized structure of roles makes it easier to update, debug, and maintain automation code. 

4. #### Shareability:
Roles can be shared with others, either within an organization or through platforms like Ansible Galaxy, facilitating collaboration and knowledge sharing.

5. #### Scalability:
Roles enable teams to scale their automation efforts by providing a consistent and repeatable way to manage infrastructure and applications. 

In essence, roles help you write cleaner, more efficient, and more maintainable Ansible playbooks, especially for larger and more complex projects. 

### Directory Structure of an Ansible Role

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
