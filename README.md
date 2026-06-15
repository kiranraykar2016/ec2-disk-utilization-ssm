# ec2-disk-utilization-ssm
# EC2 Disk Utilization Monitoring Using AWS Systems Manager

## Project Overview

This project demonstrates how to monitor disk utilization on an Amazon EC2 instance using AWS Systems Manager (SSM) without requiring SSH access.

The objective was to:

* Configure AWS Systems Manager access
* Verify EC2 instance management through SSM
* Execute disk utilization commands remotely
* Analyze storage consumption
* Provide capacity planning recommendations

---

## Architecture

EC2 Instance
↓
IAM Role (AmazonSSMManagedInstanceCore)
↓
AWS Systems Manager
↓
Run Command
↓
Disk Utilization Analysis

---

## Services Used

* Amazon EC2
* AWS Systems Manager (SSM)
* IAM Roles
* SSM Run Command
* Amazon Linux

---

## Implementation Steps

### 1. IAM Role Configuration

Created an IAM role and attached:

AmazonSSMManagedInstanceCore

Attached the role to the EC2 instance.

### 2. Systems Manager Verification

Verified that the EC2 instance appeared under:

Systems Manager → Managed Nodes

### 3. Disk Utilization Check

Executed remote commands using:

df -h

and

du -sh /*

through SSM Run Command.

### 4. Analysis

Reviewed:

* Root volume usage
* Available disk space
* Large directories consuming storage

---

## Findings

* EC2 instance successfully managed through SSM
* Disk utilization information collected without SSH access
* Storage capacity reviewed for future growth planning

---

## Recommendations

* Configure CloudWatch alarms for disk usage
* Schedule automated SSM commands
* Review storage trends periodically
* Expand EBS volumes proactively when required

---

## Report

Download the complete report:

[EC2 Disk Utilization Report](./ec2-disk-utilization-report-v2.pdf)

---

## Author

Kiran Raykar
Senior Technical Support Engineer

