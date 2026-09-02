<div align="center">

# ☁️ EverShop — AWS Cloud E-Commerce Deployment

**Production-grade e-commerce infrastructure on AWS**

[![AWS](https://img.shields.io/badge/AWS-Cloud-FF9900?style=for-the-badge&logo=amazonwebservices&logoColor=white)](https://aws.amazon.com)
[![EC2](https://img.shields.io/badge/EC2-Compute-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white)](https://aws.amazon.com/ec2/)
[![RDS](https://img.shields.io/badge/RDS-Database-527FFF?style=for-the-badge&logo=amazonrds&logoColor=white)](https://aws.amazon.com/rds/)
[![S3](https://img.shields.io/badge/S3-Storage-569A31?style=for-the-badge&logo=amazons3&logoColor=white)](https://aws.amazon.com/s3/)
[![CloudFront](https://img.shields.io/badge/CloudFront-CDN-8C4FFF?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/cloudfront/)

A complete AWS cloud infrastructure project that deploys a scalable, secure, and globally accessible e-commerce web application using industry best practices.

*Built as part of the NullClass Internship Program*

---

</div>

## 🏗️ Architecture Overview

```
                    ┌─────────────┐
                    │   Route 53  │  ← Custom Domain + DNS
                    │   + ACM     │  ← SSL/TLS Certificate
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │ CloudFront  │  ← Global CDN
                    │   (CDN)     │
                    └──────┬──────┘
                           │
                ┌──────────┼──────────┐
                │                     │
         ┌──────▼──────┐      ┌──────▼──────┐
         │    ALB       │      │     S3      │
         │ (Load Bal.)  │      │  (Static)   │
         └──────┬──────┘      └─────────────┘
                │
        ┌───────┼───────┐
        │               │
  ┌─────▼─────┐  ┌─────▼─────┐
  │   EC2 #1  │  │   EC2 #2  │  ← Auto Scaling Group
  │  (App)    │  │  (App)    │
  └─────┬─────┘  └─────┬─────┘
        │               │
        └───────┬───────┘
                │
         ┌──────▼──────┐
         │    RDS      │
         │ (Database)  │
         └─────────────┘
```

## ⚡ AWS Services Used

| Service | Purpose |
|---------|---------|
| **Amazon EC2** | Application hosting on virtual servers |
| **Amazon RDS** | Managed relational database (MySQL/PostgreSQL) |
| **Amazon S3** | Static asset storage (images, media, backups) |
| **Elastic Load Balancer** | Distributes traffic across EC2 instances |
| **Auto Scaling** | Automatically adjusts capacity based on demand |
| **Amazon CloudFront** | Global CDN for low-latency content delivery |
| **Route 53** | DNS management and custom domain routing |
| **AWS ACM** | SSL/TLS certificate for HTTPS encryption |

## 🔧 Key Components Implemented

### 1. 🖥️ EC2 + RDS Integration
- Launched EC2 instances with the EverShop e-commerce application
- Connected to RDS for persistent, managed database storage
- Configured security groups for secure communication

### 2. 🛒 E-Commerce Application Deployment
- Full-stack EverShop application deployed and configured
- Product catalog, shopping cart, and checkout functionality
- Admin dashboard for inventory management

### 3. 📦 Amazon S3 Integration
- Static assets served from S3 buckets
- Configured bucket policies and access controls
- Lifecycle rules for cost-optimized storage

### 4. ⚖️ Auto Scaling & Load Balancing
- Application Load Balancer for intelligent traffic distribution
- Auto Scaling Group with health checks and scaling policies
- Handles traffic spikes without manual intervention

### 5. 🌐 Domain & SSL Configuration
- Custom domain setup via Route 53
- SSL/TLS certificate provisioned through ACM
- HTTPS enforced across all endpoints

### 6. 🚀 CloudFront CDN
- Global content distribution for fast load times
- S3 origin integration for static content
- Edge caching for improved performance worldwide

## 📊 Outcome

✅ Deployed a **secure, auto-scalable, and globally accessible** e-commerce platform  
✅ Integrated database, application, storage, and networking services  
✅ Followed **AWS Well-Architected Framework** best practices  
✅ Demonstrated hands-on expertise in production-grade cloud infrastructure  

## 📄 Documentation

Detailed step-by-step documentation with screenshots is available in [`AWS.docx`](AWS.docx).

## 🛠️ Technologies

<p>
  <img src="https://img.shields.io/badge/Amazon_EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white" />
  <img src="https://img.shields.io/badge/Amazon_RDS-527FFF?style=flat-square&logo=amazonrds&logoColor=white" />
  <img src="https://img.shields.io/badge/Amazon_S3-569A31?style=flat-square&logo=amazons3&logoColor=white" />
  <img src="https://img.shields.io/badge/CloudFront-8C4FFF?style=flat-square&logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Route_53-8C4FFF?style=flat-square&logo=amazonroute53&logoColor=white" />
  <img src="https://img.shields.io/badge/Auto_Scaling-FF9900?style=flat-square&logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Load_Balancer-8C4FFF?style=flat-square&logo=awselasticloadbalancing&logoColor=white" />
  <img src="https://img.shields.io/badge/ACM-DD344C?style=flat-square&logo=amazonaws&logoColor=white" />
</p>

---

<div align="center">

**Built with ☁️ by [Aryan](https://github.com/Aryan-del-07)**

</div>