# AWS-course

 IAM (Identity and Access Management): IAM is service. It is use solved the Authentication and Authorization.
 
* What are users, policies and groups?
  Users means create a account to authentication and policies means granting some permissions to the user for authorization and groups means to resloved the create the polices to ever user we just create a group and add that user in that policy group.
 * what is Roles?
   roles are similar to user but not user because roles are mostly created for the temporary purpose, and the other way it is used to create for talking                        to one account to other aws account.
   
IAM user creating steps:

 ->step:1 Go to the console page and login into it. then click on the users and name it, and click on provide access to user, and click on the I want to create Iam user, and 
 coming to password the autogenerated password is better, so click on it.
 <img width="938" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/db9f2923-9afb-450b-bc06-7179fc0b0234">
 
 ->step:2 Add permission here go to attach permission then choose the policies.
 <img width="960" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/79dbaa2c-e0db-45e9-8ddb-e09f99447367">

 ->step:3 click on create. After then download the .csv file.
 <img width="960" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/56bccb85-69c8-47b6-a4d7-12084c62c911">

 ->step:4 Then, finally the IAM user was created.
 <img width="956" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/6981bcf8-2f76-4a58-8ae2-04d608f1263f">
 <img width="947" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/7eef08ab-75cf-418a-9341-2c4f5c96e499">


Now created the Groups:

  Go to user groups -create the group and name it as example like testinggroup, -add users, -add permissions, -click on create group.
  Here the group is ready.
 <img width="958" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/56312023-a167-4355-9441-ad17712a7a6a">









# EC2

Steps to create the instance:
  
 name the instances 
       |
 choose the operating system 
       |
 <img width="958" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/2b267774-3f52-41da-8a79-0996b17cf8cb">

 choose instance type 
       |
 create key pair 
       |
  <img width="959" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/a6cd97c9-3dfa-46da-ae31-81927be78ba0">

 network settings 
       |
  <img width="959" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/6202fe80-793d-4979-85d7-7e6de2844272">
  
 configure the storage 
       |
 lanuch instance
 <img width="959" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/f6212459-c891-4f07-ba07-0d7f8bef429d">

 Then here instance is ready.
 <img width="946" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/f53c815e-47ba-4459-8a01-225bc4a7bae7">


If we want to open the instance in the windows then install mobaxterm in the windows
<img width="956" alt="image" src="https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/ff4bf5a5-a90a-45a6-a239-462da1f6b813">

After install it open the mobaxterm - After it .....

 step1:open the mobaxterm and enter the command " ssh -i keyfilename.pem os(type)@privateIP of the EC2 "

 step2: command " <chmod680 keyfilename.pem " and Now, deploy the jenkin into the ubuntu(OStype).

 step3: Go to jenkin officals page goto unbuntu  and  install openjdk-11-jdk in mobaxterm.

 step4: copy the code from the jenkin offically page(weekly release).

 step5: command " systemCtl status jenkins " and copy the public ip address of EC2.

 step6: open the browser and enter the " http:publicip:8080 "

 step7: And go to mobaxterm means ubuntu and enter the command " cat/var/lib/jenkins/secrets/initalAdminPassword " and then copy the key and enter in the browser.
       







# VPC

A VPC is a virtual network that you create in the cloud. It allows you to have your own private section of the internet, just like having your own network within a larger network. Within this VPC, you can create and manage various resources, such as servers, databases, and storage.

Think of it as having your own little "internet" within the bigger internet. This virtual network is completely isolated from other users' networks, so your data and applications are secure and protected.

Just like a physical network, a VPC has its own set of rules and configurations. You can define the IP address range for your VPC and create smaller subnetworks within it called subnets. These subnets help you organize your resources and control how they communicate with each other.

To connect your VPC to the internet or other networks, you can set up gateways or routers. These act as entry and exit points for traffic going in and out of your VPC. You can control the flow of traffic and set up security measures to protect your resources from unauthorized access.

With a VPC, you have control over your network environment. You can define access rules, set up firewalls, and configure security groups to regulate who can access your resources and how they can communicate.

![image](https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/09b7554e-960d-4b95-bcf3-bf1c79ad982d)

By default, when you create an AWS account, AWS will create a default VPC for you but this default VPC is just to get started with AWS. You should create VPCs for applications or projects.

# VPC components

Virtual private clouds (VPC): A VPC is a virtual network that closely resembles a traditional network that you'd operate in your own data center. After you create a VPC, you can add subnets.

Subnets: A subnet is a range of IP addresses in your VPC. A subnet must reside in a single Availability Zone. After you add subnets, you can deploy AWS resources in your VPC.

IP addressing: You can assign IP addresses, both IPv4 and IPv6, to your VPCs and subnets. You can also bring your public IPv4 and IPv6 GUA addresses to AWS and allocate them to resources in your VPC, such as EC2 instances, NAT gateways, and Network Load Balancers.

Network Access Control List (NACL): A Network Access Control List is a stateless firewall that controls inbound and outbound traffic at the subnet level. It operates at the IP address level and can allow or deny traffic based on rules that you define. NACLs provide an additional layer of network security for your VPC.

Security Group: A security group acts as a virtual firewall for instances (EC2 instances or other resources) within a VPC. It controls inbound and outbound traffic at the instance level. Security groups allow you to define rules that permit or restrict traffic based on protocols, ports, and IP addresses.  

Routing: Use route tables to determine where network traffic from your subnet or gateway is directed.

Gateways and endpoints: A gateway connects your VPC to another network. For example, use an internet gateway to connect your VPC to the internet. Use a VPC endpoint to connect to AWS services privately, without the use of an internet gateway or NAT device.

Peering connections: Use a VPC peering connection to route traffic between the resources in two VPCs.

Traffic Mirroring: Copy network traffic from network interfaces and send it to security and monitoring appliances for deep packet inspection.

Transit gateways: Use a transit gateway, which acts as a central hub, to route traffic between your VPCs, VPN connections, and AWS Direct Connect connections.

VPC Flow Logs: A flow log captures information about the IP traffic going to and from network interfaces in your VPC.

VPN connections: Connect your VPCs to your on-premises networks using AWS Virtual Private Network (AWS VPN).

# Resources
VPC with servers in private subnets and NAT

![image](https://github.com/venkataniharbillakurthi/AWS-course/assets/84034294/8fd3a83e-b435-4cfb-b421-7303efc3c963)
