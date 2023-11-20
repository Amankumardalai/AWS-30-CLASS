# AWS-30-CLASS


# What is Amazon EC2?
Amazon Web service offers EC2 which is a short form of Elastic Compute Cloud (ECC) it is a cloud computing service offered by the Cloud Service Provider AWS. You can deploy your applications in EC2 servers without any worrying about the underlying infrastructure. You configure the EC2-Instance in a very secure manner by using the VPC, Subnets, and Security groups. You can scale the configuration of the EC2-instance you have configured based on the demand of the application by attaching the autoscaling group to the EC2-instance. You can scale up and scale down the instance based on the incoming traffic of the application.  

# Why is AWS EC2 important?
You don’t require any hardware units
Easily scalable (up or down)
You only pay for what you use
You have complete control
Highly secure
You can access your assets from anywhere in the world

# Use Cases of Amazon EC2
>Deploying Application: In the AWS EC2 instance, you can deploy your application like .jar,.war, or .ear application without maintaining the underlying infrastructure.

>Scaling Application: Once you deployed your web application in the EC2 instance know you can scale your application based upon the demand you are having by scaling the AWS EC2-Instance.

>Deploying The ML Models: You can train and deploy your ML models in the EC2-instance because it offers up to 400 Gbps), and storage services purpose-built to optimize the price performance for ML projects.

>Hybrid Cloud Environment: You can deploy your web application in EC2-Instance and you can connect to the database which is deployed in the on-premises servers.

>Cost-Effective: Amazon EC2-instance is cost-effective so you can deploy your gaming application in the Amazon EC2-Instances


# Amazon EC2 Pricing

Amazon EC2 instances are priced per second according to five different options:

>On-demand
>Spot instances (discounted short-term capacity if available)
>Savings Plans (commitment to a certain amount of usage)
>Reserved Instances (discounted reserved long-term capacity)
>Dedicated Hosts (on-demand hourly or by reserved instances)


# What is the AWS EC2 Instance Types?
Here are different types of EC2 Instances:

>General Purpose Instances
>Compute Optimized Instances
>Memory-Optimized Instances
>Accelerated Computing Instances
>Storage Optimized Instances

# Type #1 - General Purpose Instances
Among the most popular and widely used EC2 instance types, the General Purpose instance is a good choice if you are new to cloud computing or AWS in general. As this instance type offers a wide balance of computing power, memory, and storage, it is suited for a majority of AWS workloads.
General-purpose instances are mostly utilized in services related to web servers, mobile or gaming development environments or apps, or enterprise-level applications like ERP or CRM. Another major distinction among general-purpose instances is the use of Fixed EC2 instances and Burstable instances – where you can scale up your overall computing power at an extra cost.
> EX:A1 instance,M5 instance,T3/ T3a instance
>
# Type #2 - Compute Optimized Instances
As the name suggests, compute-optimized instances are used during compute-intensive workloads that can benefit from processors with high computing power. Compute-optimized instances deliver high performance at a cost-effective price and are typically used in applications like web servers and scientific modeling.

>EX:C5/ C5n instance, C6/ C6g instance
>
# Type #3 - Memory-Optimized Instances
As the name suggests, memory-optimized instances are used for memory-intensive workloads that are required to process large datasets at a fast speed. Examples of memory-intensive applications include Big Data analytics or those running on Hadoop or Apache Spark.

> R5/ R5a/ R5n instance,R6g/ R6gd instance,X1/ X1e instance,High memory instance
>
# Type #4 - Accelerated Computing Instances
Accelerated Computing instances use additional hardware accelerators like Graphics Processing Units (or GPUs) and Field Programmable Gate Arrays (or FPGAs) that enable higher throughput in compute-intensive applications with more parallelism. For example, with GPU-powered instances, applications can access NVIDIA GPUs that have thousands of computing cores. 

Similarly, FPGA-powered instances provide applications with access to large FPGAs with millions of parallel logic cells.

This instance type is suitable for applications that require parallel processing. This includes graphic processing, floating-point calculators, and data pattern matching.

> EX: P3 instance,P2 instance, Inf1 instance,G3 instance,G4 instance,F1 instance
>
# Type #5 - Storage Optimized Instances
As the name suggests, storage-optimized instances are used for applications that have high storage requirements, particularly with sequential read-and-write applications like log processing. Storage-optimized instances are designed to deliver a high number of low latency and random I/O operations each second (or IOPS).

Storage-optimized instances are also suitable for cloud-running applications that run high transaction and low latency workloads in use cases such as in-memory databases, data warehousing, and data analytics.

> EX: D2 instance,H1 instance,l3/ l3en instance
>



# 1. Create an AWS account 

2. Set up an EC2 instance

3. 2a) Choosing an AMI (Amazon Machine Image):

An AMI is a template that is used to create a new instance—or virtual machine—based on user requirements. The AMI will contain information about the software, operating system, volume, and access permissions. There are two types of AMIs:

i) Predefined AMIs: Amazon creates these, and the user can modify them.

ii) Custom AMIs: The user also creates these, and they can be reused. These AMIs are also available in the AMI Marketplace 

2b) Choosing an instance type:

An instance type specifies the hardware specifications that are required in the machine from the previous step. Instance types belong to five main families:

i) Compute-optimized: For situations that require a lot of processing power 

ii) Memory-optimized: For setting up something to do with your in-memory cache

iii) GPU optimized: For setting up a gaming system, or something with the requirement of a large graphic

iv) Storage optimized: When you need to set up a storage server

v) General-purpose: When everything is equally balanced

Instance types are fixed, and their configurations cannot be altered. 

2c) Configure Instance:

You have to specify the number of instances, purchasing options, the kind of network, the subnet, assign a public IP, set the IAM role, the shutdown behavior, etc. On that note, stopping the system and terminating the system under ‘Shutdown behavior’ are completely different things.

Stopping = Temporarily shutting down the system

Terminating = Returning control to Amazon

Under the advanced details, users can also add bootstrap scripts that are executed when the virtual machine starts up. It also offers multiple payment options, such as: 

i) On-demand instances: Can be launched whenever the user requires normal rates

ii) Reserved instances: These instances are reserved for one year or three years. The entire amount has to be paid upfront or over a span of a few months.

iii) Spot instances: Bidding goes to the bidder with the highest bid. These instances are available at a lesser cost than on-demand instances.


2d) Adding Storage: 

You’re tasked with deciding the type of storage, which could be: 

i) Ephemeral Storage (temporary and free)  

ii) Amazon Elastic Block Store (permanent and paid) 

iii) Amazon S3

The size (in GBs), volume type, where the disk is mounted, and whether the volume needs to be encrypted needs to be specified. Free users get to access up to 30 GBs of SSD or magnetic storage (which can be found under ‘Volume Type’).

2e) Adding tags: 

This helps to identify instances more quickly. 

2f) Configuring security groups: 

These are used to specify rules based on which users are given access to the EC2 instance. You set up the type of security, protocol, the port range, and source (from where the incoming traffic is coming from). Incoming traffic has to be explicitly specified, and outgoing traffic is open.

2g) Review

Click on ‘Launch’ and the instance is created. However, there’s a little more work to be done. 





