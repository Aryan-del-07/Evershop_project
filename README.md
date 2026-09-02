# EverShop — AWS Cloud E-Commerce Deployment

Production deployment of an e-commerce web application on AWS, using core services for scalability, security, and global content delivery.

*Built as part of the NullClass Internship Program.*

---

## What This Is

A complete AWS infrastructure setup for hosting an e-commerce platform. The project covers the full deployment pipeline: compute, database, storage, load balancing, auto-scaling, CDN, DNS, and SSL — following AWS best practices.

This isn't application code — it's an **infrastructure project**. The focus is on how to architect and deploy a production-grade web application on AWS.

---

## Architecture

```
                    ┌─────────────┐
                    │   Route 53  │  ← Custom Domain + DNS
                    │   + ACM     │  ← SSL/TLS Certificate
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │ CloudFront  │  ← Global CDN
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
  └─────┬─────┘  └─────┬─────┘
        └───────┬───────┘
         ┌──────▼──────┐
         │    RDS      │
         │ (Database)  │
         └─────────────┘
```

---

## AWS Services Used

| Service | Role in the Architecture |
|---------|------------------------|
| **EC2** | Application servers running EverShop |
| **RDS** | Managed relational database (MySQL/PostgreSQL) |
| **S3** | Static asset storage — images, media, backups |
| **Application Load Balancer** | Distributes traffic across EC2 instances |
| **Auto Scaling Group** | Adjusts instance count based on demand |
| **CloudFront** | CDN for low-latency content delivery at the edge |
| **Route 53** | DNS management and custom domain routing |
| **ACM** | SSL/TLS certificate provisioning for HTTPS |

---

## What Was Implemented

### 1. EC2 + RDS Integration
- Launched EC2 instances with the EverShop application
- Connected to RDS for persistent database storage
- Configured security groups for controlled access between tiers

### 2. S3 Integration
- Static assets served from S3 buckets
- Configured bucket policies and access controls
- Set up lifecycle rules for storage cost optimization

### 3. Load Balancing + Auto Scaling
- Application Load Balancer for traffic distribution
- Auto Scaling Group with health checks and scaling policies
- Handles traffic spikes without manual intervention

### 4. DNS + SSL
- Custom domain via Route 53
- SSL/TLS certificate through ACM
- HTTPS enforced across all endpoints

### 5. CloudFront CDN
- S3 origin for static content
- Edge caching for global performance
- Integrated with the ALB for dynamic content

---

## Documentation

Step-by-step setup documentation with screenshots is available in [`AWS.docx`](AWS.docx).

---

## Outcome

- Deployed a secure, auto-scalable e-commerce platform accessible globally
- Integrated compute, database, storage, networking, and CDN services
- Followed AWS Well-Architected Framework principles
- Documented the entire process for reproducibility

---

## License

MIT