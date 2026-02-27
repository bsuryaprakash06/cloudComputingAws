# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: Surya Prakash B
* **Register Number**: 212224230281
* **Date of Submission**: 13 - 02 - 2026

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

## Workflow: Amazon EC2 Lab

1. **Launch Instance**  
   Create an EC2 instance named *Web Server*, select Amazon Linux AMI, choose `t2.micro`, configure the security group, enable termination protection, and add the user-data script to install the web server.

2. **Monitor Instance**  
   Ensure the instance reaches **Running (2/2 checks passed)** and review status checks, CloudWatch monitoring metrics, system logs, and instance screenshot.

3. **Configure Access**  
   Update the security group to allow **HTTP (port 80)** inbound traffic and access the web page using the instance’s public IPv4 address.

4. **Resize Resources**  
   Stop the instance, change the instance type to **t2.small**, enable stop protection, increase the EBS volume size (8 GiB → 10 GiB), and restart the instance.

5. **Test Limits and Protection**  
   Explore EC2 service quotas, test stop protection by attempting to stop the instance, disable stop protection if required, stop the instance, and submit the lab.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1874" height="1054" alt="image" src="https://github.com/user-attachments/assets/f4dbe154-88d8-40b4-af59-54f92e0bc56f" />


---

### Screenshot 2: SSH Connection to Instance

<img width="1873" height="1056" alt="image" src="https://github.com/user-attachments/assets/44e0d767-2216-4507-8521-37447c85c386" />


---

### Screenshot 3: Instance Monitoring / Status

![i-013eb4037135eed9f](https://github.com/user-attachments/assets/cffe948b-e22b-4ed5-bbed-b5b61443b803)


---

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
