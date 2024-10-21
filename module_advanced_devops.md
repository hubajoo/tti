# Advanced Module - DevOps Workbook

## Linux

### What kind of virtualization technologies are you familiar with?
Virtualization technologies allow you to run multiple virtual machines on a single physical machine. Some common ones are:

	•	VMware: A widely used virtualization software for running multiple operating systems on a single machine.
	•	VirtualBox: An open-source virtualization software that allows you to run multiple operating systems.
	•	KVM (Kernel-based Virtual Machine): A virtualization module in the Linux kernel that allows it to function as a hypervisor.
	•	Docker: A platform for developing, shipping, and running applications in containers, which are lightweight, standalone packages of software.

### What command line text manipulation tools are you familiar with?
Here are some powerful command line text manipulation tools in Linux:

	•	grep: Searches for patterns in files.
	•	awk: A programming language for text processing and data extraction.
	•	sed: A stream editor for modifying text in a pipeline.
	•	cut: Removes sections from each line of files.
	•	sort: Sorts lines of text files.
	•	uniq: Reports or omits repeated lines.
	•	tr: Translates or deletes characters.
	•	wc: Counts words, lines, and characters.

### How would you schedule a command to run every Sunday at midnight?
To schedule a command to run every Sunday at midnight, you can use cron. Here’s how you do it:

	1.	Open the crontab file for editing:
 crontab -e

 Add the following line to the file:
 0 0 * * 0 /path/to/your/command

 This means “run the command at minute 0, hour 0, every day of the month, every month, only on Sunday”.

### How would you check the available resources (memory, disk space, CPU)?
To check available resources, you can use these commands:
	•	Memory:
 free -h

 	•	Disk space:
  df -h

  •	CPU usage:
  top or htop
   

### What are hard links and symbolic links?
	•	Hard links: These are direct references to the physical data on the disk. Multiple hard links to a file point to the same inode. If you delete one hard link, others still provide access to the file.
	•	Symbolic links (symlinks): These are shortcuts or pointers to the actual file or directory. If you delete the original file, the symlink becomes broken and doesn’t work.


### What are services in the context of Linux?
In Linux, services (or daemons) are background processes that start at boot time or on-demand and perform specific tasks. Common examples include web servers (like Apache), database servers (like MySQL), and networking services (like SSH).

### Describe the permission model of Linux! How would you make a file only readable and writable by its owner?
Linux uses a permission model based on three types of access:

	•	Read (r): Allows viewing the contents of the file.
	•	Write (w): Allows modifying the contents of the file.
	•	Execute (x): Allows running the file as a program.

These permissions are set for three categories of users:

	•	Owner: The user who owns the file.
	•	Group: Users who are part of the file’s group.
	•	Others: All other users.

To make a file only readable and writable by its owner:
chmod 600 filename

### What is the difference between Gi, Gb and GB?
	•	GiB (Gibibyte): 1 GiB = 2^30 bytes = 1,073,741,824 bytes.
	•	Gb (Gigabit): 1 Gb = 10^9 bits = 1,000,000,000 bits.
	•	GB (Gigabyte): 1 GB = 10^9 bytes = 1,000,000,000 bytes.

### What are some well-known configuration files on a Linux OS?
Some well-known configuration files include:

	•	/etc/passwd: User account information.
	•	/etc/shadow: Secure user account information.
	•	/etc/group: Group account information.
	•	/etc/fstab: File system mount information.
	•	/etc/hosts: Static table lookup for hostnames.
	•	/etc/network/interfaces: Network configuration (on Debian-based systems).
	•	/etc/resolv.conf: DNS server configuration.
	•	/etc/ssh/sshd_config: SSH server configuration.

### Explain the "set" builtin command and some of its most commonly used flags!
The set command in bash is used to change the value of shell options and positional parameters. Commonly used flags include:

	•	set -e: Exit immediately if a command exits with a non-zero status.
	•	set -u: Treat unset variables as an error when substituting.
	•	set -x: Print commands and their arguments as they are executed.
	•	set -o: Enables or disables various shell options. For example, set -o noclobber prevents overwriting files.

## Networking

### What is a MAC address?
A MAC (Media Access Control) address is a unique identifier assigned to network interfaces for communications on the physical network segment. It is a 48-bit address usually represented as six pairs of hexadecimal digits, such as 00:1A:2B:3C:4D:5E.

### What is the difference between binding to 127.0.0.1 or 0.0.0.0?
	•	127.0.0.1: This is the loopback address, and binding to it means the service will only be accessible from the local machine.
	•	0.0.0.0: This represents all IPv4 addresses on the local machine, and binding to it means the service will be accessible from any network interface.

### What are the Layers of the OSI model?
The OSI (Open Systems Interconnection) model has seven layers:

	1.	Physical: Deals with the physical connection between devices.
	2.	Data Link: Handles error detection and correction from the physical layer.
	3.	Network: Manages data addressing and delivery between networks (e.g., IP).
	4.	Transport: Ensures error-free data transfer between hosts (e.g., TCP, UDP).
	5.	Session: Manages sessions between applications.
	6.	Presentation: Translates data between the application and network formats.
	7.	Application: Interfaces with the end user and applications (e.g., HTTP, FTP).

### What is the difference between a router and a switch?
	•	Router: Connects multiple networks together and routes data between them. It operates at the Network layer (Layer 3) of the OSI model.
	•	Switch: Connects devices within the same network, using MAC addresses to forward data to the correct destination. It operates at the Data Link layer (Layer 2).

### What is the difference between TCP and UDP?
	•	TCP (Transmission Control Protocol): Connection-oriented, ensures reliable data transfer with error checking, flow control, and retransmission.
	•	UDP (User Datagram Protocol): Connectionless, faster but does not guarantee delivery, order, or error checking.


### What is a VPN?
A VPN (Virtual Private Network) creates a secure, encrypted connection over a less secure network, such as the internet. It provides privacy and security by masking the user’s IP address and encrypting all data transferred between the user’s device and the VPN server.

### What is DNS?
DNS (Domain Name System) translates human-readable domain names (e.g., www.example.com) into IP addresses that computers use to identify each other on the network.

### What is DHCP?
DHCP (Dynamic Host Configuration Protocol) dynamically assigns IP addresses and other network configuration parameters to devices on a network, allowing them to communicate with other IP networks.

### What are some well-known ports?
	•	HTTP: Port 80
	•	HTTPS: Port 443
	•	FTP: Port 21
	•	SSH: Port 22
	•	Telnet: Port 23
	•	SMTP: Port 25
	•	DNS: Port 53
	•	POP3: Port 110
	•	IMAP: Port 143


### What are the private IP address ranges?
	•	Class A: 10.0.0.0 - 10.255.255.255
	•	Class B: 172.16.0.0 - 172.31.255.255
	•	Class C: 192.168.0.0 - 192.168.255.255

### How many usable addresses are in 192.168.1.0/24?
In a /24 subnet, there are 256 total IP addresses. Subtracting 1 for the network address and 1 for the broadcast address, there are 254 usable IP addresses.

### What network diagnostic/debugging tools are you familiar with?
	•	ping: Tests the reachability of a host.
	•	traceroute/tracert: Traces the path packets take to a host.
	•	nslookup: Queries DNS to obtain domain name or IP address mapping.
	•	dig: DNS lookup utility.
	•	netstat: Displays network connections, routing tables, interface statistics.
	•	tcpdump: Captures and analyzes network packets.
	•	Wireshark: Network protocol analyzer.

### What is the purpose of the ARP protocol?
ARP (Address Resolution Protocol) maps an IP address to a physical MAC address on a local network. It allows devices to find the MAC address associated with an IP address to communicate within the same network.

### What are the basic networking components in AWS?
	•	VPC (Virtual Private Cloud): Isolated network environment in the cloud.
	•	Subnets: Segments of a VPC, where you can launch AWS resources.
	•	Internet Gateway: Allows communication between the VPC and the internet.
	•	NAT Gateway: Enables instances in a private subnet to connect to the internet or other AWS services but prevents the internet from initiating connections with those instances.
	•	Route Tables: Controls the routing of traffic within the VPC.
	•	Security Groups: Virtual firewalls for your instances to control inbound and outbound traffic.
	•	Network ACLs: Additional layer of security that acts as a firewall for controlling traffic in and out of subnets.
	•	Elastic IPs: Static IP addresses for dynamic cloud computing.
	•	VPN Gateway: Enables you to establish a secure connection between your VPC and your data center or home network.

## Security

### What is encryption at rest and encryption in transit, and how are these implemented in AWS?

	•	Encryption at rest: Protects data stored on disks from unauthorized access. In AWS, this can be implemented using services like:
	•	Amazon S3: Server-side encryption (SSE) with options like SSE-S3, SSE-KMS, and SSE-C.
	•	Amazon EBS: Encrypted volumes using AWS KMS keys.
	•	RDS: Encrypted databases with AWS KMS.
	•	Encryption in transit: Protects data as it travels across the network. In AWS, this is implemented using:
	•	TLS/SSL: Encrypts data in transit for services like Amazon S3, Amazon RDS, and other web-based services.
	•	VPN: Secure connections using AWS Site-to-Site VPN or AWS Client VPN.
	•	AWS Direct Connect: Can be combined with VPN for secure network connections.

### Which service is responsible for monitoring and log collection in AWS?
  • Amazon CloudWatch: Monitors AWS resources and applications, collecting and tracking metrics, and generating alarms.
	•	AWS CloudTrail: Tracks and logs API calls and account activity across AWS services.


### What is a bastion host, and how can it be implemented in AWS?
A bastion host is a special-purpose server used to access private instances in a VPC securely. It acts as a jump server or gateway. In AWS, it can be implemented by:

	•	Launching an EC2 instance in a public subnet with SSH/RDP access.
	•	Configuring security groups to allow access only from specific IP addresses.
	•	Using the bastion host to SSH/RDP into instances in private subnets.

### What are the key differences between security groups and NACLs?
	•	Security Groups:
	•	Operate at the instance level.
	•	Stateful: If you allow an inbound rule, the response traffic is automatically allowed.
	•	Only allow rules (no deny rules).
	•	Network ACLs (NACLs):
	•	Operate at the subnet level.
	•	Stateless: Rules are evaluated independently for inbound and outbound traffic.
	•	Allow both allow and deny rules.

### Which service is responsible for tracking activities on an AWS account?
	•	AWS CloudTrail: Provides logging, monitoring, and tracking of API calls and account activity across AWS services.

### Explain the difference between symmetric and asymmetric encryption!
	•	Symmetric Encryption:
	•	Uses the same key for encryption and decryption.
	•	Faster and more efficient for large amounts of data.
	•	Example: AES (Advanced Encryption Standard).
	•	Asymmetric Encryption:
	•	Uses a pair of keys: a public key for encryption and a private key for decryption.
	•	More secure for key exchange but slower.
	•	Example: RSA (Rivest-Shamir-Adleman).

### What is the Principle of Least Privilege, and how can it be implemented in AWS?
The Principle of Least Privilege states that users and systems should only have the minimum level of access necessary to perform their tasks. In AWS, this can be implemented by:

	•	Creating IAM policies that grant only the permissions required for specific roles or users.
	•	Regularly reviewing and updating permissions.
	•	Using IAM roles for temporary access with time-limited permissions.

### How do AWS IAM roles differ from IAM users, and in what scenarios would you use each?
	•	IAM Users: Represent a single person or service and have long-term credentials (username/password, access keys). Used for individual access to AWS services.
	•	IAM Roles: Do not have long-term credentials. Instead, they provide temporary security credentials. Used for granting permissions to AWS services, applications, or other AWS accounts.
Scenarios:
	•	Use IAM Users for employees needing access to the AWS Management Console.
	•	Use IAM Roles for EC2 instances, Lambda functions, or cross-account access where temporary credentials are needed.

### Explain the AWS Shared Responsibility Model in the context of security.
The AWS Shared Responsibility Model outlines the division of security responsibilities between AWS and the customer:

	•	AWS Responsibilities (Security “of” the cloud):
	•	Physical security of data centers.
	•	Hardware and software infrastructure.
	•	Network infrastructure.
	•	Managed services like RDS, DynamoDB.
	•	Customer Responsibilities (Security “in” the cloud):
	•	Data encryption and integrity.
	•	Identity and access management (IAM).
	•	Configuration of security settings.
	•	Network configurations.
	•	Application-level security.

## Containers and container orchestration

### What are the key differences between containers and virtual machines?
	•	Containers:
	•	Share the host operating system kernel.
	•	Are lightweight and have faster startup times.
	•	Are more resource-efficient.
	•	Typically used for packaging and deploying applications.
 
	•	Virtual Machines (VMs):
	•	Include a full operating system, including the kernel.
	•	Are heavier and take longer to start.
	•	Are more resource-intensive.
	•	Typically used for running multiple different operating systems on the same hardware.


### What are the most important instructions in a Dockerfile?
	•	FROM: Specifies the base image.
	•	RUN: Executes commands in the container during the image build process.
	•	CMD: Sets the default command to run when a container starts.
	•	ENTRYPOINT: Configures a container to run as an executable.
	•	COPY/ADD: Copies files from the host system to the container.
	•	WORKDIR: Sets the working directory for the container.
	•	ENV: Sets environment variables.
	•	EXPOSE: Documents which ports the container will listen on at runtime.

### What is the difference between the CMD and the ENTRYPOINT instructions?
	•	CMD:
	•	Provides default arguments for the ENTRYPOINT instruction or specifies the default command to run if no command is provided.
	•	Can be overridden with docker run arguments.
 
	•	ENTRYPOINT:
	•	Configures a container to run as an executable, defining the command that will always run.
	•	Is not overridden by docker run arguments, but arguments can be appended to the ENTRYPOINT command.

### How does caching work in docker builds?
Docker uses a layer caching mechanism. Each instruction in a Dockerfile creates a layer, and Docker caches these layers. If a layer has not changed, Docker will reuse the cached layer instead of rebuilding it, speeding up the build process. Changes to earlier layers invalidate subsequent layers, necessitating a rebuild of those layers.

### What are some common practices for optimizing container image size?
	•	Use minimal base images (e.g., alpine instead of ubuntu).
	•	Remove unnecessary files and dependencies.
	•	Use multi-stage builds to reduce the final image size.
	•	Minimize the number of layers by combining commands in RUN.
	•	Clean up package manager caches and temporary files.

### What problems can occur when the "latest" tag is used? 
	•	Unpredictable Behavior: “latest” might point to different versions over time, leading to inconsistencies.
	•	Dependency Issues: Other images or services might rely on specific versions.
	•	Debugging Difficulties: Harder to reproduce issues when “latest” changes.
	•	Deployment Problems: Potential for deploying untested changes.

### Explain the architecture of a Kubernetes cluster!
A Kubernetes cluster consists of:

	•	Master Node (Control Plane):
	•	API Server: Exposes the Kubernetes API.
	•	Etcd: Stores all cluster data.
	•	Controller Manager: Manages controllers that regulate the state of the cluster.
	•	Scheduler: Assigns pods to nodes based on resource availability.
	•	Worker Nodes:
	•	Kubelet: Agent that ensures containers are running in pods.
	•	Kube-proxy: Manages network rules and load balancing.
	•	Container Runtime: Runs containers (e.g., Docker, containerd).

### What is the Deployment Kubernetes object responsible for?
A Deployment manages the desired state of applications. It provides declarative updates for pods and ReplicaSets, ensuring a specified number of replicas are running. It supports rolling updates and rollbacks.

### What kind of probes are there in Kubernetes, and what are their use cases?
	•	Liveness Probe: Checks if the application is running. If it fails, Kubernetes restarts the container.
	•	Readiness Probe: Checks if the application is ready to serve traffic. If it fails, the container is removed from service endpoints.
	•	Startup Probe: Checks if the application has started. It is used for slow-starting containers to distinguish between startup failures and regular liveness issues.

### What is the difference between resource Limit and Request?
	•	Resource Request: The amount of CPU/memory guaranteed to a container. Used for scheduling decisions.
	•	Resource Limit: The maximum amount of CPU/memory a container can use. Prevents a container from using too many resources.

### What is the Service Kubernetes object responsible for?
A Service provides a stable network endpoint for accessing a set of pods. It abstracts pod IP addresses, enabling communication within the cluster. Services can be of types like ClusterIP, NodePort, LoadBalancer, and ExternalName.

### What are the main differences between ConfigMaps and Secrets?
	•	ConfigMaps:
	•	Store non-sensitive configuration data as key-value pairs.
	•	Can be used to manage environment variables, command-line arguments, or configuration files.
	•	Data is stored in plain text.
 
	•	Secrets:
	•	Store sensitive data, such as passwords, tokens, and keys.
	•	Data is base64-encoded and can be encrypted at rest.
	•	Provides better security practices for managing sensitive information.

## Infrastructure as Code

### What is Infrastructure as Code? What are its advantages and disadvantages?
Infrastructure as Code (IaC) is the practice of managing and provisioning computing infrastructure using machine-readable definition files, rather than physical hardware configuration or interactive configuration tools.

Advantages:

	•	Consistency: Ensures consistent configurations across environments.
	•	Version Control: Infrastructure definitions can be versioned and managed similarly to application code.
	•	Automation: Reduces manual effort and human error through automation.
	•	Scalability: Easily scales infrastructure up or down.
	•	Reproducibility: Enables identical infrastructure setups across multiple environments (development, testing, production).

Disadvantages:

	•	Complexity: Initial setup and learning curve can be complex.
	•	Debugging: Troubleshooting IaC scripts can be challenging.
	•	Maintenance: Keeping IaC scripts updated with evolving infrastructure can require ongoing effort.
	•	Dependencies: External dependencies (e.g., cloud provider APIs) might introduce reliability concerns.
 
### What are the basic commands of the terraform workflow?
	•	terraform init: Initializes a working directory containing Terraform configuration files.
	•	terraform plan: Creates an execution plan, showing what actions Terraform will take to achieve the desired state.
	•	terraform apply: Applies the changes required to reach the desired state of the configuration.
	•	terraform destroy: Destroys the infrastructure managed by Terraform.
	•	terraform fmt: Formats the configuration files to a canonical format.
	•	terraform validate: Validates the configuration files for syntax errors.

### What is the difference between resources and data sources in terraform?
Resources: Define the components (e.g., virtual machines, networks, databases) that Terraform will manage. They describe the desired state of infrastructure.
hcl
resource "aws_instance" "example" {
  ami           = "ami-12345678"
  instance_type = "t2.micro"
}

	•	Data Sources: Allow Terraform to fetch data from existing infrastructure. They are used to query existing resources and use their attributes in your configuration.
 hcl
 data "aws_ami" "example" {
  most_recent = true
  owners      = ["self"]
}

### What does state mean in the context of terraform?
State in Terraform refers to a snapshot of the infrastructure managed by Terraform. It keeps track of the resources and their attributes so that Terraform can map real-world resources to your configuration, keep track of metadata, and improve performance.

### What are modules in terraform?
Modules are containers for multiple resources that are used together. A module consists of a collection of .tf files in a directory. They help organize and reuse code, making configurations more manageable and scalable.

hcl
module "vpc" {
  source = "./modules/vpc"
  cidr_block = "10.0.0.0/16"
}

### List the meta-arguments in terraform with their use cases!

	•	count: Allows you to manage multiple resources based on a count.
 resource "aws_instance" "example" {
  count = 3
  ...
}

	•	for_each: Creates multiple resources from a map or set.
 resource "aws_instance" "example" {
  for_each = toset(["one", "two", "three"])
  ...
}

	•	depends_on: Specifies dependencies between resources.
 resource "aws_instance" "example" {
  depends_on = [aws_vpc.example]
  ...
}


	•	provider: Specifies which provider configuration to use for a resource.
 resource "aws_instance" "example" {
  provider = aws.west
  ...
}

	•	lifecycle: Manages resource creation, update, and deletion behavior.
 resource "aws_instance" "example" {
  lifecycle {
    prevent_destroy = true
  }
  ...
}


### What is the best practice for a terraform project's file structure?
A well-structured Terraform project typically follows these practices:

	•	Separate Directories for Environments:

 ├── environments
│   ├── dev
│   │   └── main.tf
│   ├── prod
│   │   └── main.tf
└── modules
    ├── vpc
    │   └── main.tf
    ├── ec2
    │   └── main.tf

	•	Modules:
	•	Place reusable components (modules) in their own directories.
	•	Environment Configuration:
	•	Separate configurations for different environments (e.g., development, production).
	•	State Files:
	•	Store state files remotely, such as in an S3 bucket with state locking enabled using DynamoDB.
	•	Version Control:
	•	Store all configuration files in a version control system like Git.

