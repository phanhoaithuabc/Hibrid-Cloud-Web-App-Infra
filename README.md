# Hibrid-Cloud-Web-App-Infra

Our fictitious company is called The E-Commerce Company.

After a failure in our datacenter, the CEO has demanded our team come up with a better solution to prepare and handle such failure events moving forward and mitigate the downtime it caused our customers. You are given the job to design a private cloud solution for your company’s key revenue generator, an e-commerce web application.

According to your CEO, all of the VMs must be protected against failure.

### Read the e-mail below to understand the specific configurations necessary to be set to meet the business requirements.

CTO E-mail
Hello,

It has come to our attention that our main revenue producing application stack is no longer able to meet the company's needs for performance and availability. We have been considering a Hyperconverged solution with continuing plans to expand into the cloud in the future. We have acquired an HCI cluster to do a proof of concept.

We have interviewed all the business stakeholders and determined their processing needs; the next step is for you to build out a test solution for evaluation.

We would like to see a 3-tier application stack with a database server VM, application server VM and web server VM. Identified requirements are to have separate production and development environments. The production environment requires built-in data protection using backup/restore with snapshots and no more than 1 hour of data loss after a failure. Additional tests for VM workload expansion (cloning), the ability to dynamically add CPU/Memory resources to online virtual machines (add 1 vCPU and 2GB memory to the database server) is required. Final verification is the removal of a key VM and performing a full restoration.

The systems administration group has provisioned the test environment HCI cluster. You will be responsible for the basic infrastructure configurations and virtual machine buildout and testing. The applications team will perform the database and application installations. Our CEO would like to see a demo tomorrow - you have 8 hours to prepare the environment. I'm sure you're up to the task!

Respectfully, CTO

### Read the e-mail below to understand the specific configurations necessary to be set to meet the business requirements.
Hi!

The network infrastructure will consist of separate production and development networks. The production network will be managed using IPAM/DHCP from an IP Pool provided by the Network Operations group. The production network will be on vlan 0, using the 172.31.0.0/24 network. The IP Pool will use a Start address of 172.31.0.210 and an End address of 172.31.0.230. The development network will be unmanaged on VLAN 101 using the 172.31.101.0/24 network.

Respectfully, Network Operations

### Read the e-mail below to understand the specific configurations necessary to be set to meet the business requirements.
Hey there!

The basic testing resource requirements for each virtual machine in the 3-tier application stack will be the same. Microsoft SQL on Windows, has been chosen for the database tier and the application server and web server tiers will both be Linux based. Each virtual machine will be configured with 1 vCPU and 4 GB of RAM. For testing purposes you will need to configure the Network Time Protocol (NTP) using the public service, pool.ntp.org, and 8.8.8.8 for the Domain Naming Service (DNS). You will also need to create a new storage container called Images to hold the Windows and CentOS virtual disk images (C:\Images) to be uploaded to the Image Service. The virtual machine naming convention will be based on a 2-3 letter representation, followed by the environment. Example: Database server for Production, use db-prod. Application for development, use app-dev, etc…

The production virtual machines, when created based on the previous criteria, should be duplicated to create an identical development environment.

Respectfully, Systems Administration

### Directions
Refer to the e-mails provided in the project to set the correct configurations for the following:

1. The NTP server to the HCI Cloud Platform.
2. The Name Server to the HCI Cloud Platform.
3. A managed virtual network using IPAM/DHCP in the HCI Cloud Platform.
4. An unmanaged virtual network in the HCI Cloud Platform.
5. A storage container to the HCI Cloud Platform and upload Windows and Linux (CentOS) virtual disk images to the new container.
5. Deploying Windows and Linux virtual machines in the HCI Cloud Platform.
6. Creating virtual machine clones and change configurations in the HCI Cloud Platform.
7. Creating data protection configurations to automate virtual machine snapshots.
8. Performing virtual machine restorations using the data protection snapshots.

### Project Submission Directions
After you have set the configurations as directed on the previous Project Workspace page, follow the steps below when you are ready to submit your project.

1. Open a text editor and compose an email message to the CTO. The contents of the email should include a summary of the stakeholder needs and an outline of the tasks performed. This text email file will be included in your project submission.

2. You will need the information shown below to capture your cluster configuration for project submission. In your project workspace, in the Frame Desktop, open the Password.txt file and use only the values highlighted below when prompted.