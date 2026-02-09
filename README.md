# Secure Multi-Tier VPC Architecture on AWS

## Overview
Designed and deployed a production-ready multi-tier VPC on AWS following security best practices and the AWS Well-Architected Framework.

## Architecture Components

### Network Design
- **VPC**: Custom VPC (10.0.0.0/16) spanning 3 Availability Zones for high availability
- **Public Subnets**: Host NAT Gateway and Internet-facing resources
- **Private Subnets**: Host application servers and databases with no direct internet access

### Security
- **Security Groups**: Stateful firewall rules controlling inbound/outbound traffic at instance level
- **Network ACLs**: Stateless subnet-level firewall for defense in depth
- **Internet Gateway**: Enables internet access for public subnet resources
- **NAT Gateway**: Allows private subnet instances to access internet for updates while remaining private

### Monitoring & Logging
- **VPC Flow Logs**: Captures IP traffic information for troubleshooting and security analysis
- **CloudWatch Integration**: Centralized log monitoring and analysis

### Private Connectivity
- **VPC Endpoint (S3)**: Gateway endpoint for private S3 access without internet gateway traversal
- Eliminates data transfer costs and improves security posture

## Key Features
- Multi-AZ deployment for fault tolerance
- Separation of public and private network tiers
- Least privilege network access controls
- Comprehensive traffic logging and monitoring
- Cost-optimized private AWS service access

## Skills Demonstrated
- AWS VPC networking and subnetting
- Security group and NACL configuration
- Route table management
- Network troubleshooting with Flow Logs
- AWS service integration (S3, CloudWatch)

## Tools Used
- AWS Console
- AWS CLI
- CloudWatch for monitoring

---

**Note**: This was a learning project. Resources were deployed temporarily and terminated to avoid charges.
