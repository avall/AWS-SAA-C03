* [Return to table of contents](../../README.md)
# Introduction to Virtual Private Cloud (VPC)
## Pre-knowledge
- [Basic Networking](./000a-basic-networking.md)
- [CIDR — Classless Inter-Domain Routing](./003-ec2.md#34-cidr--classless-inter-domain-routing)

## Introduction
- A VPC is an isolated network space where we can define logical public & private subnets across multiple availability zones in the same region.
- The only way to access the VPC from: Internet, Private VPN connection, External locations
is adding gateway services.
- VPC provides a logically isolated section of the AWS Cloud where you can define your own virtual network environment.
- Multiple VPCs can coexist within a single AWS region, with a soft limit of 5 VPCs per region.

## Domain Model
![VPC Domain Model](../uml/004-vpc/vpc-domain-model.svg)

## Internet Gateway

## Route tables
- Each VPC has a default route table called the main route table.


## Subnet
- The private subnets are accessible from Internet, private VPN connection or external network location because we have:
  - Gateway Services 
  - Route Tables
defined in the VPC. 

