# **AWS Interview Questions & Answers**

1. **Q: List the components required to build Amazon VPC?**

    - **Ans:** Subnet, Internet Gateway, NAT Gateway, HW VPN Connection, Virtual Private Gateway, Customer Gateway, Router, Peering Connection, VPC Endpoint for S3, Egress-only Internet Gateway.

1. **Q: How do you safeguard your EC2 instances running in a VPC?**

    - **Ans:** Security Groups can be used to protect your EC2 instances in a VPC. We can configure both INBOUND and OUTBOUND traffic in a Security Group which enables secured access to your EC2 instances. Security Group automatically denies any unauthorized access to your EC2 instances.

1. **Q: In a VPC how many EC2 instances can you use?**

    - **Ans:** Initially you are limited to launch 20 EC2 Instances at one time. Maximum VPC  size is 65,536 instances.

1. **Q:** **Can you establish a peering connection to a VPC in a different REGION?**

    - **Ans:** You can establish peering relationships between VPCs across different AWS Regions (also called inter-Region VPC peering).

1. **Q: Can you connect your VPC with a VPC owned by another AWS account?**

    - **Ans:** Yes, Possible. Provided the owner of other VPCs accepts your connection.

1. **Q: What are all the different connectivity options available for your VPC?**

    - **Ans:** Internet Gateway, Virtual Private Gateway, NAT, EndPoints, Peering Connections.

1. **Q: Can a EC2 instance inside your VPC connect with the EC2 instance belonging to other VPCs?**

    - **Ans:** Yes, Possible. Provided an Internet Gateway is configured in such a way that traffic bounded for EC2 instances running in other VPCs.

1. **Q: How can you monitor network traffic in your VPC?**

    - **Ans:** It is possible using Amazon VPC Flow-Logs feature.

1. **Q: Difference between Security Groups and ACLs in a VPC?**

    - **Ans:** A Security Group defines which traffic is allowed TO or FROM  EC2 instance. Whereas ACL, controls at the SUBNET level, scrutinize the traffic TO or FROM a Subnet.

1. **Q: Hon an EC2 instance in a VPC establish the connection with the internet?**

    - **Ans:** Using either a Public IP or an Elastic IP.

1. **Q: Different types of Cloud Computing as per services?**

    - **Ans:**  PAAS (Platform As A Service), IAAS (Infrastructure As A Service), SAAS (Software As A Service)

1. **Q: What is Auto Scaling?**

    - **Ans:** Creating duplicate instances during heavy business hours. Scale-IN and Scale-OUT are two different statues of Scaling. Scale-IN: Reducing the instances. Scale-OUT: Increasing the instances by duplicating.

1. **Q: What is AMI?**

    - **Ans:** AMI is defined as Amazon Machine Image. Basically it’s a template comprising software configuration part. For example, Operating System, DB Server, Application Server, etc.,

1. **Q: Difference between Stopping and Terminating the Instances?**

    - **Ans:** When you STOP an instance it is a normal shutdown. The corresponding EBS volume attached to that instance remains attached and you can restart the instance later. When you TERMINATE an instance it gets deleted and you cannot restart that instance again later. And any EBS volume attached with that instance also deleted.

1. **Q: When you launch a standby Relational Database Service instance will it be available in the same Available Zone?**

    - **Ans:** Not advisable. Because the purpose of having standby RDS  instance is to avoid an infrastructure failure. So you have to keep your standby RDS service in a different Availability Zone, which may have different infrastructure.

1. **Q: Difference between Amazon RDS, DynamoDB and Redshift?**

    - **Ans:** RDS is meant for structured data only. DynamoDB is meant for unstructured data which is a NoSQL service. Redshift is a data warehouse product used for data analysis.

1. **Q: What are Lifecycle Hooks?**

    - **Ans:** Lifecycle Hooks are used in Auto Scaling. Lifecycle hooks enable you to perform custom actions by pausing instances as an Auto Scaling group launches or terminates them. Each Auto Scaling group can have multiple lifecycle hooks.

1. **Q: What is S3?**

    - **Ans:** S3 stands for Simple Storage Service, with a  simple web service interface to store and retrieve any amount of data from anywhere on the web.

1. **Q: What is AWS Lambada?**

    - **Ans:** Lambda is an event-driven platform. It is a compute service that runs code in response to events and automatically manages the compute resources required by that code.

1. **Q: In S3 how many buckets can be created?**

    - **Ans:** By default 100 buckets can be created in a region.

1. **Q: What is CloudFront?**

    - **Ans:** Amazon CloudFront is a service that speeds up transfer of your static and dynamic web content such as HTML files, IMAGE files., etc., CloudFront delivers your particulars thru worldwide data centers named Edge Locations.

1. **Q: Brief about S3 service in AWS?**

    - **Ans:** S3, a Simple Storage Service from Amazon. You can move your files TO and FROM S3. Its like a FTP storage. You can keep your SNAPSHOTS in S3. You can also ENCRYPT your sensitive data in S3.

1. **Q: Explain Regions and Available Zones in EC2?**

    - **Ans:** Amazon has hosted EC2 in various locations around the world. These locations are called REGIONS. For example in Asia, Mumbai is one region and Singapore is another region. Each region is composed of isolated locations which are known as AVAILABLE ZONES.    Region is independent. But the Available Zones are linked thru low-latency links.

1. **Q: What are the two types  of Load Balancer?**

    - **Ans:** Classic LB and Application LB. ALB is the Content Based Routing.

1. **Q: Can a AMI be shared?**

    - **Ans:** Yes. A developer can create an AMI and share it with other developers for their use. A shared AMI is packed with the components you need and you  can customize the same as per your needs. As you are not an owner of a shared AMI there is a risk always involved.

1. **Q: What is a Hypervisor?**

    - **Ans:** A Hypervisor is a kind of software that enables Virtualization. It combines physical hardware resources into a platform which is delivered virtually to one or more users. XEN is the Hypervisor for EC2.

1. **Q: Key Pair and its uses?**

    - **Ans:** You use Key Pair to login to your Instance in a secured way. You can create a key pair using EC2 console. When your instances are spread across regions you need to create key pair in each region.

1. **Q: What is the feature of ClassicLink?**

    - **Ans:** ClassicLink allows instances in EC2 classic platform to communicate with instances in VPC using Private IP address. EC2 classic platform instances cannot not be linked to more than one VPC at a time.

1. **Q: Can you edit a Route Table in VPC?**

    - **Ans:** Yes. You can always modify route rules to specify which subnets are routed to the Internet gateway, the virtual private gateway, or other instances.

1. **Q: How many Elastic IPs can you create?**

    - **Ans:** 5 VPC Elastic IP addresses per AWS account per region

1. **Q: Can you ping the router or default gateway that connects your subnets?**

    - **Ans:** NO, you cannot. It is not supported. However you can ping EC2 instances within a VPC, provided your firewall, Security Groups and network ACLs allows such traffic.

1. **Q: How will you monitor the network traffic in a VPC?**

    - **Ans:** Using Amazon VPC Flow Logs feature.

1. **Q: Can you make a VPC available in multiple Available Zones?**

    - **Ans:** Yes.

1. **Q: How do you ensure an EC2 instance is launched in a particular Available Zone?**

    - **Ans:** After selecting your AMI Template and Instance Type, in the third step while configuring the instance you must select the SUBNET in which you wish to launch your instance. It will be launched in the AZ associated with that SUBNET.

1. **Q: For Internet Gateways do you find any Bandwidth constraints?**

    - **Ans:** NO. Normally an IG is HORIZONTALLY SCALLED, Redundant and Highly Available. It is not having nay Bandwidth constraints usually.

1. **Q: What is the significance of a Default VPC?**

    - **Ans:** When you launch your instances in a Default VPC in a Region, you would be getting the benefit of advanced Network Functionalities. You can also make use of Security Groups, multiple IP addresses, and multiple Network interfaces.

1. **Q: Can you make use of default EBS Snapshots?**

    - **Ans:** You can use, provided if it is located in the same region where your VPC is presented.

1. **Q: What will happen when you delete a PEERING CONNECTION in your side?**

    - **Ans:** The PEERING CONNECTION available in the other side would also get terminated. There will no more traffic flow.

1. **Q: Can you establish a Peering connection to a VPC in a different region?**

    - **Ans:** NO. Its possible between VPCs in the same region.

1. **Q: Can you connect your VPC with a VPC created by another AWS account?**

    - **Ans:** Yes. Only when that owner accepts your peering connection request.

1. **Q: When you delete your DB instance what will happen to your backups and DB snapshots?**

    - **Ans:** When a DB instance is deleted, RDS retains the user-created DB snapshot along with all other manually created DB snapshots. Also automated backups are deleted and only manually created DB Snapshots are retained.

1. **Q: What is the significance of an Elastic IP?**

    - **Ans:** The Public IP is associated with the instance until it is stopped or terminated Only. A Public IP is not static. Every time your instance is stopped or terminated the associated Public IP gets vanished and a new Public IP gets assigned with that instance. To over come this issue a public IP can be replaced by an Elastic IP address, which stays with the instance as long as the user doesn’t manually detach it. Similarly when if you are hosting multiple websites on your EC2 server, in that case you may require more than one Elastic IP address.

1. **Q: How will you use S3 with your EC2 instances?**

    - **Ans:** Websites hosted on your EC2 instances can load their static contents directly from S3. It provides highly scalable, reliable, fast, inexpensive data storage infrastructure.

1. **Q: Is this possible to connect your company datacenter to Amazon Cloud?**

    - **Ans:** Yes, you can very well do this  by establishing a VPN connection between your company’s network and Amazon VPC.

1. **Q: Can you change the Private IP of an EC2 instance while it is running or stopped?**

    - **Ans:** A Private IP is STATIC. And it is attached with an instance throughout is lifetime and cannot be changed.

1. **Q: What is the use of Subnets?**

    - **Ans:** When a network has more number of HOSTS, managing these hosts can be tedious under a single large network. Therefore we divide this large network into easily manageable sub-networks (subnets) so that managing hosts under each subnet becomes easier.

1. **Q: What is the use of Route Table?**

    - **Ans:** Route Table is used to route the network pockets. Generally one route table would be available in each subnet. Route table can have any no. of records or information, hence attaching multiple subnets to a route table is also possible.

1. **Q: Can you use the Standby DB instance for read and write along with your Primary DB instance?**

    - **Ans:** Standby server cannot be used in parallel with primary server unless your Primary instance goes down.

1. **Q: What is the use of Connection Draining?**

    - **Ans:** Connection Draining is a service under Elastic Load Balancing. It keeps monitoring the healthiness of the instances. If any instance fails Connection Draining pulls all the traffic from that particular failed instance and re-route the traffic to other healthy instances.

1. **Q: What is the role of AWS CloudTrail?**

    - **Ans:** CloudTrail is designed for logging and tracking API calls. Also used to audit all S3 bucket accesses.

1. **Q: What is the use of Amazon Transfer Acceleration Service?**

    - **Ans:** ATA service speeds up your data transfer with the use of optimized network paths. Also, speed up your CDN up to 300% compared to normal data transfer speed

1. **Q: You cannot store unlimited data in Amazon Web Services…..**

    1.  True
    2.  False

    - **Ans:** False

1. **Q:** **Rapid provisioning allows you to very quickly spin up a new virtual machine with minimal effort. True or false ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: A hybrid setup is one in which part of your resources are AWS and the rest are with another cloud provider. True or False ?**

    1.  True
    2.  False

    - **Ans:** False

1. **Q:** **As an added layer of security for AWS management, which of the following should be you do ?**

    1.  Create multiple Admin accounts
    2.  Generate a new security key each time you log in
    3.  Create IAM users

    - **Ans:** Create IAM users

1. **Q: Is AMI template ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: EC2 Instances are Virtual Server in AWS**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: What does “elastic” refer to in Elastic Compute Cloud(EC2)? Select all that apply.**
    1.  Increasing and decreasing capacity as needed
    2.  Monitoring services on multiple devices
    3.  Operating on Mac, Windows and Linux
    4.  Paying only for running virtual machines
    5.  Stretching applications across virtual machines

    - **Ans:** 1. Increasing and decreasing capacity as needed & 4. Paying only for running virtual machines

1. **Q: You can upload a custom configuration virtual image and sell it on the AWS Marketplace. True or false ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: EC2 Machine types define which of the following ?**

   1.  AWS Region
    2.  Core Count
    3.  User Location

    - **Ans:** Core Count

1. **Q: Which is default instance type**

    1.  On-demand
    2.  RI
    3.  Spot instance

    - **Ans:** On-demand

1. **Q: What is Elastic Computing ?**

    1.  Data will be replicate to different AZs
    2.  You can spin up and spin down VMs
    3.  Automatically VMs will be add and remove

    - **Ans:** You can spin up and spin down VMs

1. **Q:** **You can upload a custom configuration virtual image and sell it on the AWS Marketplace. True or false ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: EC2 Machine types define which of the following ?**

    1.  AWS Region
    2.  Core Count
    3.  User Location

    - **Ans:** Core Count

1. **Q:** **Which is default instance type**

    1.  On-demand
    2.  RI
    3.  Spot instance

    - **Ans:** On-demand

1. **Q: What is Elastic Computing ?**

    1.  Data will be replicate to different AZs
    2.  You can spin up and spin down VMs
    3.  Automatically VMs will be add and remove

    - **Ans:** You can spin up and spin down VMs

1. **Q: Can We launch multiple instances with same AMI ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: PEM file is one time physical password…**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Windows user required PPK file to connect Linux instance hosted on AWS.**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: You can purchase time on EC2 directly from other users and specify the price you want to pay. True or false ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Which of the following might prevent your EC2 instance from appearing in the list of instances?**

    1.  EC2 is not selected
    2.  Correct region is not selected
    3.  AWS marketplace is not selected

    - **Ans:** Correct region is not selected

1. **Q: Which of the following main reason to terminate an unused EC2 instance ?**

    1.  Security Concerns
    2.  Additional fees
    3.  Data Loss

    - **Ans:** Additional fees

1. **Q: Which AWS service exists only to redundantly cache data and images ?**

    1.  AWS Availability Zones
    2.  AWS Edge Locations
    3.  AWS Regions

    - **Ans:** AWS Edge Locations

1. **Q: Regions, AZs and Edge Locations all terms are same…**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: AWS every service is available at every regions….**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: Premium support is Available in AWS for Developer, Business & Enterprise level ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Can you add new Debit/Credit card in your AWS Account ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Can you increase micro to large of instance ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: On-demand instances is based on a bid mechanism.**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: RI can be sold on the AWS marketplace?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Which is default types options in AWS?**

    1.  On-demand
    2.  RI
    3.  Spot instance

    - **Ans:** On-demand

1. **Q: What are On-demand, RI and Spot instances ? Which instance is best on Production?**

    1.  On-demand
    2.  RI
    3.  Depends on Application or Website

    - **Ans:** Depends on Application or Website

1. **Q: Which is most expensive options in instance ?**

    1.  On-demand
    2.  RI
    3.  Spot instance

    - **Ans:** On-demand

1. **Q: Amazon S3  is internet accessible storage via HTTP /HTTPS**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Amazon S3 is not a object level of storage**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: Amazon S3 is storage for the Internet**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Temporary storage access speed is not guaranteed.**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: There is 99.99% SLA(Service Level Agreement) for temporary storage.**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: Ephemeral storage is block-level storage ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Single object size is up to 5 TB in Amazon S3.**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: You can create unlimited bucket size in Amazon S3.**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: By default, Instance-Backed and EBS-Backed root volumes delete all data. However, when using EBS-Backed storage, you can configure it to save the data on the root volume. True or false ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: You can switch from an Instance-Backed to an EBS-Backed root volume at  any time. True or False ?**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: When using an EBS-Backed machine, you can override the terminate option and save the root volume. True or False ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Which of the following is a service of AWS Simple Storage Service(S3)? Select all that apply.**

    1.  Database Indexing
    2.  File searching
    3.  Secure Hosting
    4.  Storage Scaling

    - **Ans:** 3. Secure Hosting & 4. Storage Scaling

1. **Q: What’s the difference between instance store and EBS?**

    **Issue**

    I’m not sure whether to store the data associated with my Amazon EC2 instance in instance store or  in an attached Amazon Elastic Block Store (Amazon EBS) volume. Which option is best for me?

    - **Ans:** **Resolution**

    Some Amazon EC2 instance types come with a form of directly attached, block-device storage known as the instance store. The instance store is ideal for temporary storage, because the data stored in instance store volumes is not persistent through instance stops, terminations, or hardware failures. You can find more detailed information about the instance store at Amazon EC2 Instance Store.

    For data you want to retain longer-term, or if you need to encrypt the data, we recommend using EBS volumes instead. EBS volumes preserve their data through instance stops and terminations, can be easily backed up with EBS snapshots, can be removed from instances and reattached to another, and support full-volume encryption. For more detailed information about EBS volumes, see Features of Amazon EBS.

1. **Q: BS can be attached to any running instance that is in the same Availability Zone ?**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: EBS is  internet accessible**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: EBS has persistent file system for EC2**

    1.  True
    2.  False

    - **Ans:** True

1. **Q:** **EBS supports incremental snapshots**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Amazon Glacier enables customers to offload the administrative burdens of operating and scaling storage to AWS.**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Amazon Glacier is a great storage choice when low storage cost is paramount.**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Data is rarely retrieved, and retrieval latency of several hours is acceptable in Glacier**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Glacier is basically for data archival**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: It is very cheap storage**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Glacier has very, very slow retrieval times**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: By Default, Instance-Backed and EBS-Backed root volumes delete all data. However, when using EBS-Backed storage, you can configure it to save the data on the root volume.**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: You can switch from an Instance-Backed to an EBS-Backed root volume at any time.**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: When using an EBS-Backed machine, you can override the terminate option and save the root volume.**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: VPC is Private, Isolated, Virtual Network**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: VPC would be logically isolated network in AWS cloud**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: VPC is also give control of network architecture**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: VPC is also going to enhanced security**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: VPC has ability to interwork with other organizations**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: VPC does not enable hybrid cloud(site-to-site VPN)**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: Route Table is a set of Rules tells the direction of network**

    1.  True
    2.  False

    - **Ans:** True

1. **Q: Security Group is a subnet level of security**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: NACLs(Network Access Lists) is a resource level of security**

    1.  True
    2.  False

    - **Ans:** False

1. **Q: Any default stack is available in Cloud Formation ?**

    - **Ans:**  You can not create default stack but you can choose the type of stack to create e.g :

    1.  A sample stack
    2.  A Linux-based chef 12 stack
    3.  A Windows-based Chef 12.2 stack
    4.  A Linux-based Chef 11.10 stack

1. **Q: What is the difference between Stack and Template in Cloud Formation ?**

    - **Ans:** Stack : Cloud-based applications usually require a group of related resources—application servers, database servers, and so on—that must be created and managed collectively. This collection of instances is called a stack

1. **Q: We can create multiple server for same stack ?**

    - **Ans:** you can select one “instance type” e.g: t2.micro at a time but you can set more then one “Webserver Capacity” which is “The initial number of Webserver instances“ means automatically same kind of instances will launch.

1. **Q:  Can you explain the term SQS is pull based, not pushed base.**

    - **Ans:** It means that you have to actively poll the queue in order to receive a messages. The messages are pushed into the queue by the producers but pulled out of the queue by the consumers.You have to call the Receive Message action from the consumer in order to get the messages, they are not pushed to you automatically when they arrive.

1. **Q: How many Elastic IP address can be associated with a single account?**

    1.  4
    2.  10
    3.  5
    4.  None the above

    - **Ans:**

1. **Q: What is the name to the additional network interfaces that can be created and attached to any Amazon EC2 instance in your VPC?**

    1.  Elastic IP
    2.  Elastic Network Interface
    3.  AWS Elastic Interface
    4.  AWS Network ACL

    - **Ans:** Elastic Network Interface

1. **Q: You have configured ELB with three instances connected to that. If your instances are unhealthy or terminated, the traffic should be automatically replaced to another instance, what type of service can be used to achieve this requirement?**

    1.  Sticky session
    2.  Fault Tolerance
    3.  Connection drainage
    4.  Monitoring

    - **Ans:** Fault Tolerance

1. **Q: After configuring ELB, you need to ensure that the user requests are always attached to a single instance. What setting can you use?**

    1.  Session cookie
    2.  Cross one load balancing
    3.  Connection drainage
    4.  Sticky session

    - **Ans:** Sticky session

1. **Q: Which of the following metrics cannot have a cloud watch alarm?**

    1.  EC2 instance status check failed
    2.  EC2 CPU utilization
    3.  RRS lost object
    4.  Auto scaling group CPU utilization

    - **Ans:** RRS lost object

1. **Q: Which of the below mentioned service is provided by Cloud watch?**

    1.  Monitor estimated AWS usage
    2.  Monitor EC2 log files
    3.  Monitor S3 storage
    4.  Monitor AWS calls using Cloud trail

    - **Ans:** Monitor estimated AWS usage

1. **Q: A user has Launched an EC2 instance which of the below mentioned statements is not true respect to instance addressing?**

    1.  The private IP addresses are not reachable from the internet
    2.  The user can communicate using the private IP across regions
    3.  The private IP address and pubic IP address for an instance are directly mapped to each other using NAT
    4.  The private IP address for the instance is assigned using DHCP

    - **Ans:** The user can communicate using the private IP across regions

1. **Q: Which of the following service provides the edge – storage or content delivery system that caches data at different locations?**

    1.  Amazon RDS
    2.  Simple DB
    3.  Amazon Cloud Front
    4.  Amazon associates web services

    - **Ans:** Amazon Cloud Front

1. **Q: A user is launching an instance under the free usage tier from the AMI with a snapshot size of 50 GB. How can the user launch the instance under the free usage tier?**

    1.  Launch a micro instance
    2.  Launch a micro instance, but in the EBS configuration modify the size of EBS to 50 GB.
    3.  Launch a micro instance, but do not store the data of more than 30 GB on the EBS storage.
    4.  It is not possible to have this instance under the free usage tier

    - **Ans:** It is not possible to have this instance under the free usage tier

1. **Q: What are the possible connection issues you can face while connecting to your instance?**

    1.  Connection timed out
    2.  Server refused our key
    3.  No supported authentication methods available
    4.  All of the above

    - **Ans:** All of the above

1. **Q: You are enabled sticky session with ELB. What does it do with your instance?**

    1.  Routes all the requests to a single DNS
    2.  Binds the user session with a specific instance
    3.  Binds the user IP with a specific session
    4.  Provides a single ELB DNS for each IP address

    - **Ans:** Binds the user session with a specific instance

1. **Q: Which is a main email platform that provides an easy, cost effective way for you to send compliance and receive a response using your own email address and domains?**

    1.  SES
    2.  SNS
    3.  SQS
    4.  SAS

    - **Ans:** SES

1. **Q: Which type of load balancer makes routing decisions at either the transport layer or the application layer and supports either EC2 or VPC.**

    1.  Application Load Balancer
    2.  Classic Load Balancer
    3.  Primary Load Balancer
    4.  Secondary Load Balancer

    - **Ans:** Classic Load Balancer

1. **Q: AWS Cloud Front has been configured to handle the customer requests to the web server launched in Linux machine. How many requests per second can Amazon Cloud Front handle?**

    1.  1000
    2.  100
    3.  10000
    4.  There is no such limit

    - **Ans:** There is no such limit

1. **Q: You are going to launched one instance with security group. While configuring security group, what are the things you have to select?**

    1.  Protocol and type
    2.  Port
    3.  Source
    4.  All of the above

    - **Ans:** Source

1. **Q: Which is virtual network interface that you can attach to an instance in a VPC?**

    1.  Elastic IP
    2.  AWS Elastic Interface
    3.  Elastic Network Interface
    4.  AWS Network ACL

    - **Ans:** Elastic Network Interface

1. **Q: You have launched a Linux instance in AWS EC2. While configuring security group, you have selected SSH, HTTP, HTTPS protocol. Why do we need to select SSH?**

    1.  To verity that there is a rule that allows traffic from your computer to port 22
    2.  To verify that there is a rule that allows traffic from EC2 Instance to your computer
    3.  Allows web traffic from instance to your computer
    4.  Allows web traffic from your computer to EC2 instance

    - **Ans:** To verify that there is a rule that allows traffic from EC2 Instance to your computer

1. **Q: You need to quickly set up an email service because a client needs to start using it in the next hour. Amazon service seems to be the logical choice but there are several options available to set it up. Which of the following options to set up AWS service would best meet the needs of the client?**

    1.  Amazon SES console
    2.  AWS Cloud Formation
    3.  SMTP interface
    4.  AWS Elastic Beanstalk

    - **Ans:** Amazon SES console

1. **Q:You have chosen a windows instance with Classic and you want to make some change to the security group. How will these changes be effective?**

    1.  Security group rules cannot be changed
    2.  Changes are automatically applied to windows instances
    3.  Changes will be effective after rebooting the instance in that security group
    4.  Changes will be effective after 24-hours

    - **Ans:** Changes are automatically applied to windows instances

1. **Q: Load Balancer and DNS service comes under which type of cloud service?**

    1.  IAAS-Network
    2.  IAAS-Computational
    3.  IAAS-Storage
    4.  None of the above

    - **Ans:** IAAS-Storage

1. **Q: You have an EC2 instance that has an unencrypted volume. You want to create another encrypted volume from this unencrypted volume. Which of the following steps can achieve this?**

    1.  Just simply create a copy of the unencrypted volume, you will have the option to encrypt the volume.
    2.  Create a snapshot of the unencrypted volume and then while creating a volume from the snapshot you can encrypt it
    3.  Create a snapshot of the unencrypted volume (applying encryption parameters), copy the snapshot and create a volume from the copied snapshot
    4.  This is not possible, once a volume is unencrypted, there is no way to create an encrypted volume from this

    - **Ans:** Create a snapshot of the unencrypted volume (applying encryption parameters), copy the snapshot and create a volume from the copied snapshot

1. **Q: Where does the user specify the maximum number of instances with the auto scaling commands?**

    1.  Auto scaling Launch Config
    2.  Auto scaling group
    3.  Auto scaling policy
    4.  Auto scaling size

    - **Ans:** Auto scaling Launch Config

1. **Q: A user is identify that a huge data download is occurring on his instance he has already set the auto scaling policy to increase the instance count when the network Input Output increase beyond a threshold limits how can the user ensure that this temporary event does not result in scaling**

    1.  The network I/O are not affecting during data download
    2.  The policy cannot be set on the network I/O
    3.  There is no way the can stop scaling as it already configured
    4.  Suspend scaling

    - **Ans:** Suspend scaling

1. **Q: Which are the types of AMI provided by AWS?**

    1.  EBS Backed
    2.  Instance Store backed
    3.  None its volume type and not AMI types
    4.  Both A and B

    - **Ans:** Both A and B
