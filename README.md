# Zach-Project-1
Project 1 Azure
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagramproject_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._ 

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly _secure____, in addition to restricting __access___ to the network.
- _TODO: What aspect of security do load balancers protect? defends against DDos attacks What is the advantage of a jump box?_ used as an origination point to connect to other servers or untrusted enviroments

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _____ and system _____.
- _TODO: What does Filebeat watch for?_Monitors log files and locations that have been specified by the user.
- _TODO: What does Metricbeat record?_ Helps to monitor the metrics on the system; collected from services running on the server.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name      | Function     | Ip Address | Operating System |   |
|-----------|--------------|------------|------------------|---|
|           |              |            |                  |   |
| Jump Box  | Gateway      | 10.0.0.10  | Linux            |   |
| Web 1     | DVWA         | 10.0.0.20  | Linux            |   |
| Web 2     | DVWA/Docker  | 10.0.0.21  | Linux            |   |
| Elk Stack | log          | 10.1.0.4   | Linux            |   |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the __ELK_ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: 10.0.0.10 where the docker container is located.

Machines within the network can only be accessed by __SSH___.
- _TODO: Which machine did you allow to access your ELK VM?_ Web 2 What was its IP address? 10.0.0.21

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box |    No               |10.0.0.20 10.0.0.21   |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_ it allows admin's to focus on other important tasks.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker ps.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_ 10.0.0.20 and 10.0.0.21

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_ Filebeat and Metricbeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._ Metricbeat collects metrics and filebeat collects log files and log events. 

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_the ansible-plabook/ yaml file. after running the playbook it should be copied to the other machines on the network.
- _Which file do you update to make Ansible run the playbook on a specific machine? ansible-config. How do I specify which machine to install the ELK server on versus which to install Filebeat on?_They should bve installed on the same Elk machine since the Elk machine is what will be used to grab and store those logs.
- _Which URL do you navigate to in order to check that the ELK server is running?  http://[your.VM.IP]:5601/app/kibana.

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._  "ansibleplaybook whateverthefileis.yml"
