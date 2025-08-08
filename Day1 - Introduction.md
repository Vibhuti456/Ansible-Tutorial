
# Ansible Introduction

### What is Ansible? 
Ansible is an open-source IT automation tool that simplifies and automates various manual IT processes, including provisioning, configuration management, application deployment, and orchestration. It is designed to be minimal, consistent, secure, and highly reliable, with an extremely low learning curve for administrators, developers, and IT managers.

It is created by contributions from an active open-source community. Ansible is designed to be simple, powerful, and agentless, which means it does not require any software or agents to be installed on the managed nodes.

Ansible uses a declarative language called YAML to define automation tasks, which makes it easy to read and understand.

### History Of configuration

In past, we used to have system administrators in all IT companies and had their servers on-premises. System administrators had to responsible taking care of all the servers on their data center. 

Most of the servers are Windows and Linux with different distributions.

#### Responsibilites includes
1. Keep the servers up to date with all the tools such as OpenSSH, wget, curl etc.
2. Using distributions with supported version in the servers. 
3. Installing the system dependencies, application dependencies to make any application run inside the servers
4. Maintaining all the servers with resource ultilization, storage resource and availablity of the servers. 

Writting scripts to automates the tasks would not a good idea, because windows servers has different configuration and linux has different configuration which makes administrators task hard and tedious.

### Introduction to Puppet and Chef - 
Puppet and chef tools came in existence doing the same task - Task of automation.

It acts as a meduim between the administrators and servers where the tasks need to be perform. 

The prerequisites to use this tools is knowledge of Ruby language because these tools are written in Ruby language and plus knowledge of tools as well. so, the learning curve is extremely high and these tools needed an additional software or Agent on the managed node to execute the tasks.

Then Ansible Introduced for automating the task for configuration. 

## Why we used Ansible -

Ansible is used for automating IT tasks such as configuration management, application deployment, cloud provisioning, and orchestration, allowing organizations to manage complex and repetitive processes across large-scale infrastructures efficiently. It is popular because it is simple to set up, agentless (requiring no installation on target nodes), flexible, free, and helps maintain consistency and reduce manual errors in IT environments.


## How Ansible Works -  

#### Architecture: 
Ansible operates on a control node (where commands and playbooks are executed) and manages multiple managed nodes (servers or devices). The control node sends instructions over SSH (or WinRM for Windows) without needing agents installed on each managed node.

#### Inventory: 
Systems to be managed are listed in an inventory file, organized into groups if needed.

#### Modules: 
The control node pushes modules (scripts that accomplish specific tasks) to the target machines over SSH, executes them, and removes them after completion. Modules can install software, configure system settings, and perform various automation tasks.

#### Playbooks: 
Automation workflows are defined in YAML-formatted playbooks, which describe desired system states and actions—a human-readable set of instructions that Ansible follows to achieve consistent configurations.

#### Execution: 
A user runs Ansible or an Ansible playbook from the control node. Ansible reads the playbook, connects to each node listed in the inventory, executes the specified tasks by invoking one or more modules, and reports results.