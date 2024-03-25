# terraform-two-tier
It is simple deployment of application and db layer. It has simple terraform script to deploy it using code deploy tool.

This two-tier architecture will contain the following components:

Deploy a VPC with CIDR 10.0.0.0/16
Within the VPC we will have 2 public subnets with CIDR 10.0.0.0/18 and 10.0.64.0/18. Each public subnet will be in a different Availability Zone for high availability
Create 2 private subnets with CIDR ‘10.0.128.0/18’ and ‘10.0.192.0/18’ and each will be in a different Availability Zone
Deploy RDS MySQL instance.
An Application load balancer that will direct traffic to the public subnets.
Deploy one EC2 instance in each public subnet for high availability.
Internet Gateway and Elastic IPs for EC2 instance.
Prerequisites:

Install Terraform CLI
Install AWS CLI
AWS Account
Code Editor (I used VS Code for this deployment)
