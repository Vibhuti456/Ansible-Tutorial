### Error Handling in Ansible

Error handling in Ansible is primarily managed through the use of ignore_errors, failed_when, and changed_when directives. These directives allow you to control how Ansible responds to errors and determine the success or failure of a task based on specific conditions.

Let’s understand how Ansible handles errors:

1. #### ignore_errors: 
This directive allows a playbook to continue executing even if a task fails. While this can be useful in some cases, it’s important to use it judiciously, as it can mask underlying issues and lead to unexpected behaviour.

2. #### failed_when: 
With this directive, you can specify conditions under which a task should be considered failed. For example, you can use it to fail a task if a specific command returns a non-zero exit code or if a particular file is missing.
