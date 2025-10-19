AWS Cloud Infrastructure Project — E-Commerce Deployment

By Aryan Sahoo (NullClass Internship Project)

This project demonstrates full-stack deployment of an E-Commerce Web Application on AWS Cloud using various core services for scalability, security, and performance.

🔹 Project Overview

The project focuses on designing and implementing a complete AWS architecture that hosts an e-commerce platform integrated with databases, storage, CDN, load balancing, auto-scaling, and secure domain configuration.

🔹 Key Components Implemented

1.Amazon EC2 + RDS Integration

  Launched EC2 instance (Amazon Linux/Ubuntu) and configured SSH access.

  Created and connected MySQL RDS database from EC2 using CLI.

  Created tables, inserted, and verified sample data.

2.E-Commerce Application Deployment

  Deployed EverShop (Node.js + PostgreSQL) on EC2.

  Configured environment variables and PostgreSQL database.

  Hosted and ran the application using PM2 and NGINX reverse proxy for stability and public access.

3.Amazon S3 Integration

  Created an S3 bucket for storing product images.

  Configured public read access and integrated image URLs in the web app.

4.Auto Scaling and Load Balancing

  Designed Launch Templates for EC2 instance replication.

  Created an Auto Scaling Group (ASG) and Application Load Balancer (ALB) for traffic distribution and fault tolerance.

  Deployed a simple Apache web server to test scalability.

5.Domain & SSL Configuration (Route 53 + ACM)

  Registered custom domain using Route 53.

  Requested and validated SSL certificates using AWS Certificate Manager (ACM).

  Configured HTTPS traffic through ALB + CloudFront for global secure access.

6.CloudFront + S3 Integration (CDN)

Created CloudFront distribution to serve static content globally.

Restricted direct S3 access using Origin Access Control (OAC).

Tested performance improvement of CloudFront vs. S3.

🔹 Outcome

Successfully deployed a secure, auto-scalable, and globally accessible e-commerce website on AWS.

Integrated database, application, storage, and networking services following industry best practices.

Demonstrated hands-on expertise in AWS services, system configuration, and cloud-based application hosting.

🔹 Technologies Used

AWS EC2 • RDS (MySQL/PostgreSQL) • S3 • CloudFront • Route 53 • ACM • Auto Scaling • Load Balancer • NGINX • Node.js • PM2
