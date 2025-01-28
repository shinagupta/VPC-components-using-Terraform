# VPC-components-using-Terraform
Day 40 Challenge completed!! 💪

Mastering #Terraform Blocks, Providers, and Variables



🎯The Challenge:

Create a VPC with Public and Private Subnets, IGW, RT, NAT Using Terraform



What you will Learn:

1. Configure a VPC with public and private subnets in AWS using Terraform.

2. Set up Internet Gateway (IGW) and NAT Gateway for internet access.

3. Configuring route tables and associating them with subnets.

4. Output variables to display important resource information.

5. Creating Terraform components: VPC, SUBNETS, IGW, RT, NAT GATEWAY



Pre-Requisites Knowledge:

 VPC, subnets, AWS region and availability zones, CIDR Block, routing tables, Integrating Internet Gateways (IGW), NAT, Security Group



Tools Used:

VS Code editor, terraform, AWS CLI, AWS Dashboard, ChatGPT(for errors) 😄 



Steps that I followed in VS Code Editor:

1. Terraform main Block

2. Provider Block

3. Input Variables

4. Output Variables

(All the code files can be accessed for the GIT Repository:

5. Practical Task: VPC Setup

(An overview of the resources created)

Step 1: Create 🖥️ VPC (Virtual Private Cloud)

 This is your private network on the cloud. Think of it like a house where you control everything.

CIDR Block: 10.0.0.0/16

Enabled Features: DNS Hostnames ✅, DNS Resolution ✅



Step 2: Add a Public Subnet🌐

 A small room in your house where people can access the internet!

+-------------------------------+

|        🏠 VPC (10.0.0.0/16)       |

| +---------------------------+ |

| | 🌐 Public Subnet (10.0.1.0/24) | <--> 🌩️ Internet Gateway (IGW) |

| +---------------------------+ |

+-------------------------------+

CIDR Block: 10.0.1.0/24

Auto-Assign Public IP: Enabled ✅

Connected to: Internet Gateway (IGW) 🌩️



Step 3: Add a Private Subnet🔒

 Another small room in your house where only you have access!

CIDR Block: 10.0.2.0/24

Auto-Assign Public IP: Disabled ❌



Step 4: Create an Internet Gateway (IGW)🌩️

 The front door of your house, allowing internet access for the public subnet!

Public Subnet (10.0.1.0/24) <--> 🌩️ IGW <--> 🌐 Internet

Attach this Internet Gateway to your VPC!



Step 5: Add a NAT Gateway🔄

 Allows resources in the private subnet to securely access the internet without being exposed



Step 6: Configure Route Tables🗺️ 

 These are like maps that guide network traffic!

Public Route Table

Destination: 0.0.0.0/0 → 🌩️ Internet Gateway

Associated with: Public Subnet

Private Route Table

Destination: 0.0.0.0/0 → 🌀 NAT Gateway

Associated with: Private Subnet



Step 7: Outputs 📋

After Terraform runs successfully, display the following information:

VPC ID 🏠

Public Subnet ID 🌐

Private Subnet ID 🔒

Subnet CIDR Blocks 📦



I'm thrilled to have completed this challenge! #getfitwithsagar #SRELife #DevOpsForAll #terraformwithsagar"
