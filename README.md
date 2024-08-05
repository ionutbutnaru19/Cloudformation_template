**Web Application Infrastructure on AWS**


This repository contains CloudFormation templates to deploy a scalable and resilient web application infrastructure on Amazon Web Services (AWS). 
The infrastructure is designed to host a web application that consists of multiple components, including a virtual private cloud (VPC), 
public and private subnets, an internet-facing load balancer, auto-scaling group, and associated security groups.


Template will create and deploy the following resources:

1. Virtual Private Cloud (VPC) where the whole environment will be contained.
2. Internet gateway to facilitate communication between resources within the VPC and public internet.
3. Various Route tables to provide control of the network traffic between resources and subnets.
4. Two public and private subnets in two separate Availability Zones, for segmentation of the virtual private cloud and high availability of our resources.
5. Two NAT gateways with allocated Elastic IP for allowing resources in private subnets to access the public internet.
6. Two security groups, to control network traffic to and from the resources.
7. Two bastion servers, which will act as a secure entry point to access the resources in the private subnets.
8. One application load balancer with its associated components, which distributes the network traffic to the instances in the private subnets.
9. One autoscaling group which is managing and deploying EC2 instances for the web application. The autoscaling group will use a specific launch configuration, including all required software packages and files to handle external queries.
10. Cloudwatch alarms for monitoring, to scale the web servers infrastructure based on specific conditions.
