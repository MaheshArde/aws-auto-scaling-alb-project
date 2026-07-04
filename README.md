# aws-auto-scaling-alb-project
A beginner AWS project that demonstrates how to create a scalable web infrastructure using EC2, Launch Templates, Auto Scaling Groups, and an Application Load Balancer. The project shows how traffic is distributed across multiple EC2 instances and how Auto Scaling automatically adjusts resources based on CPU utilization.
# AWS Auto Scaling Group with Application Load Balancer

## 📖 Project Overview

This project demonstrates how to create a scalable web infrastructure on AWS using Auto Scaling Groups (ASG) and an Application Load Balancer (ALB).

The Auto Scaling Group automatically launches or terminates EC2 instances based on CPU utilization, while the Application Load Balancer distributes incoming traffic across healthy EC2 instances.

This project helped me understand the basic concepts of Auto Scaling, Load Balancing, and High Availability in AWS.

---

## AWS Services Used

- Amazon EC2
- Launch Template
- Auto Scaling Group (ASG)
- Application Load Balancer (ALB)
- Target Group
- Amazon CloudWatch
- Amazon VPC

---

## Architecture

```
Internet
    │
    ▼
Application Load Balancer
    │
    ▼
Target Group
    │
    ▼
Auto Scaling Group
   │      │
 EC2-1  EC2-2
```

---

##  Configuration

- **Instance Type:** t3.micro
- **Desired Capacity:** 1
- **Minimum Capacity:** 1
- **Maximum Capacity:** 5
- **Scaling Policy:** Target Tracking
- **CPU Utilization:** 40%

---

##  Testing

Install the Stress tool:

```bash
sudo apt update
sudo apt install stress -y
stress -c 50
```

When CPU utilization exceeds 40%, the Auto Scaling Group launches additional EC2 instances automatically.

---

##  Screenshots

Add your screenshots in the `screenshots` folder.

Example:

- Launch Template
- Auto Scaling Group
- Load Balancer
- Target Group
- CloudWatch
- Final Output

---

##  Project Structure

```
aws-auto-scaling-alb-project
│
├── README.md
├── screenshots/
├── architecture/
├── scripts/
└── docs/
```

---

##  What I Learned

- Creating Launch Templates
- Configuring Auto Scaling Groups
- Setting up an Application Load Balancer
- Monitoring with CloudWatch
- Testing Auto Scaling using CPU stress

---

##  Author

**Mahesh**  
BCA Final Year Student  
Learning AWS & DevOps through hands-on projects.
