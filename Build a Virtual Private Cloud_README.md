<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** Adwait Joshi  
**Email:** apjadwait.joshi93@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/intense_indigo_vibrant_tayberry/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will set up and configure a VPC ... I'm doing this project to learn how to create an Amazon VPC, a public subnet and an internet gateway

### What is Amazon VPC?

Amazon VPC is a private, isolated section of the AWS cloud where you launch resources in a virtual network you define. It gives you complete control over IP ranges, subnets, and routing. It is useful because it provides security and isolation, like having your own private data center in the cloud.

In today's project, I used Amazon VPC to create a public subnet, which then I connected to internet via internet gateway.

### Personal reflection

This project took me around 45 mins.

One thing I didn't expect in this project was the secret mission about AWS CLI.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will access the VPC console in AWS and create a VPC because to get familiar with the vital skill of setting up and managing a VPC.

### How VPCs work

VPCs are the reason why resources in AWS can be made private. It is a secure, isolated private cloud hosted within a public cloud.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because I could launch resources (e.g. EC2 instances) and connect services together from Day 1 of using AWS. This default VPC is a handy starting point, especially for beginners, but you can always create custom VPCs to fit specific requirements e.g. strict security measures.

![Image](http://learn.nextwork.org/intense_indigo_vibrant_tayberry/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is 10.0.0.0/16. Basically, to define an IPv4 CIDR block is a way to assign a whole block of IP addresses. Here, IP addresses within this CIDR block start at 10.0.0.0 and go up to 10.0.255.255 as the CIDR block size is /16.

---

## Subnets

### What I did in this step

In this step, I will launch a subnet inside the VPC because this will divide the VPC into subdivisions, which will allow to start planning where different resources will live and operate.

### Creating and configuring subnets

Subnets are subdivisions inside the VPC, used to group resources with similar access rules and restrictions. Some subnets might be public areas that all resources can access (public subnets) while others are private areas with limited access (private subnets). There are already subnets existing in my account, one for every Availability Zone of a Region

### Public vs private subnets

The difference between public and private subnets are resources inside a public subnet can communicate with external networks, whereas a private subnet does not have direct internet access. For a subnet to be considered public, it has to connect to internet.

![Image](http://learn.nextwork.org/intense_indigo_vibrant_tayberry/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 address for a subnet. This setting makes sure any EC2 instance launched in that subnet will instantly get a public IP address so that I won't have to create one manually.

---

## Internet gateways

### What I did in this step

In this step, I will connect the VPC to the internet using a internet gateway because it will allow the public subnet to access internet

### Setting up internet gateways

Internet gateways are key to making applications available on the internet. By attaching an internet gateway, your instances can access the internet and be accessible to external users.

Attaching an internet gateway to a VPC means resources in the VPC can now access the internet. The EC2 instances with public IP addresses also become accessible to users, so the applications hosted on those servers become public too. If I missed this step the VPC wouldn't connect to internet irrespective of internet gateway.

![Image](http://learn.nextwork.org/intense_indigo_vibrant_tayberry/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will use the AWS CLI to launch your VPC's resource because it is a faster, more efficient way to do this project.

### Exploring CloudShell and CLI

VPC resources could also be created with CloudShell, which is shell in the AWS Management Console, a space to run code. It already has AWS CLI pre-installed. CLI is is a software that let us create, delete and update AWS resources with commands instead of clicking through the console. It is a go-to tool use to automate tasks using scripts, making the CLI essential for managing the cloud environment in an efficient way.

### Debugging my setup

To set up a VPC or a subnet, you can use the command aws ec2 create-subnet --vpc-id VPC-ID --cidr-block ADD-CIDR-BLOCK-HERE Make sure to avoid errors by including correct VPC ID allotted and correct format of CIDR block, which would 10.0.0.0. The subnet CIDR block should be within VPC's CIDR block range.

![Image](http://learn.nextwork.org/intense_indigo_vibrant_tayberry/uploads/aws-networks-vpc_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands is that it is qucik. An advantage of using the Console is that it is having a visual guide... Overall, I preferred CLI as it save a lot of time.

---

---
