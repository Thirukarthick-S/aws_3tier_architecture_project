# AWS 3-Tier Architecture Deployment

This project demonstrates the design and deployment of a **3-Tier Architecture** on AWS, following industry best practices for scalability, high availability, and security.

---

## 📌 Architecture Overview

The application is divided into three layers:

1. **Presentation Layer (Web Tier)**  
   - Hosted on **EC2 instances** in an Auto Scaling Group (ASG).  
   - **Elastic Load Balancer (ELB)** distributes traffic across instances.  
   - **CloudFront** + **S3** used for static content hosting and caching.  

2. **Application Layer**  
   - Deployed on EC2 instances inside private subnets.  
   - Auto Scaling enabled for fault tolerance and high availability.  

3. **Database Layer**  
   - **Amazon RDS (MySQL)** with Multi-AZ deployment for redundancy and failover.  
   - **DynamoDB** optionally used for NoSQL storage.  

---

## 🛠️ Tools & Services Used

- **AWS EC2** (ASG, LB, TG)  
- **Amazon VPC** (Public & Private Subnets, NAT Gateway, Security Groups)  
- **IAM** (Roles & Policies)  
- **Amazon RDS (MySQL)**  
- **Amazon S3** (Static Hosting)  
- **Amazon CloudFront** (CDN)  
- **Amazon Route 53** (DNS Management)  
- **AWS WAF** (Web Application Firewall)  
- **Amazon CloudWatch & CloudTrail** (Monitoring & Auditing)  

---

## ⚙️ Deployment Steps

1. **Networking Setup**  
   - Create VPC with public/private subnets.  
   - Configure Internet Gateway and NAT Gateway.  
   - Set up Route Tables and Security Groups.  

2. **Presentation Layer**  
   - Launch EC2 instances in public subnet (ASG + ELB).  
   - Configure S3 bucket for static files.  
   - Attach CloudFront distribution for caching.  

3. **Application Layer**  
   - Deploy application servers in private subnet (ASG + Target Groups).  

4. **Database Layer**  
   - Launch RDS with Multi-AZ for high availability.  
   - Optionally configure DynamoDB for NoSQL data.  

5. **Security & Monitoring**  
   - Apply IAM roles and policies for least privilege.  
   - Enable WAF for security filtering.  
   - Set up CloudWatch alarms and CloudTrail for auditing.  

---

## 📊 Architecture Diagram

![AWS 3-Tier Architecture](https://github.com/Thirukarthick-S/aws_3tier_architecture_project/blob/main/assets/3TierArch.png) 

## 📊 Architecture Diagram
**OUTPUT**
![OUTPUT SCREENSHOT](https://github.com/Thirukarthick-S/aws_3tier_architecture_project/blob/main/assets/output.png)
[Lucidchart](https://www.lucidchart.com/), [Draw.io](https://app.diagrams.net/), or [Excalidraw](https://excalidraw.com/)).*  

---

## 🚀 Future Enhancements

- Integrate CI/CD pipeline with AWS CodePipeline, CodeBuild, and CodeDeploy.  
- Add containerized application layer using ECS or EKS.  
- Implement serverless features with AWS Lambda for certain functions.  

---

## 📧 Contact

Created by **Thirukarthick S**  
For queries: [your.email@example.com](iamthirukarthick@gmail.com)  
