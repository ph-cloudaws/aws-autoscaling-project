🚀 AWS Auto Scaling Project

A hands-on demo showing how to design, deploy, and test an EC2 Auto Scaling setup using Launch Templates, custom scaling limits, health checks, and automated replacement of unhealthy instances.

This project walks through the full process — step by step, with screenshots — from creating a secure environment to watching Auto Scaling replace instances in real time.

🧩 Project Overview

This project demonstrates:

Creating a Launch Template using Amazon Linux 2023

Creating an Auto Scaling Group (ASG) across multiple Availability Zones

Configuring:

Desired, minimum, and maximum capacity

Health checks and grace periods

Target tracking scaling (CPU utilization)

Triggering and validating automatic instance replacement

Visual verification through 15 screenshots stored in the images/ directory

📁 Repository Structure
aws-autoscaling-project/
│
├── images/
│   ├── asg1.png
│   ├── asg2.png
│   ├── asg3.png
│   ├── ...
│   └── asg15.png
│
└── README.md


Each image corresponds to a step in the process, from launch template configuration to validating instance replacement.

🛠️ What This Project Covers (Step-by-Step)
1️⃣ Create a Launch Template

AMI: Amazon Linux 2023

Instance type: t3.micro

No key pair (for sandbox/demonstration purposes)

Attach a security group allowing HTTPS for testing

2️⃣ Create the Auto Scaling Group

Use the launch template

Select multiple AZs (eu-west-2a, 2b, 2c)

Define initial capacity

Desired: 2

Minimum: 1

Maximum: 3

3️⃣ Configure Health Checks

EC2 health checks enabled

Grace period: 300 seconds

No load balancer for this demo

4️⃣ Add Scaling Policy

Target Tracking

Metric: Average CPU Utilization

Target value: 50%

Auto Scaling will launch or terminate instances automatically to maintain this target.

5️⃣ Observe Auto Scaling Behaviour

Terminate an instance manually

Watch Auto Scaling detect the change

A new replacement instance launches automatically

All visible in the EC2 console and documented via screenshots

🖼️ Screenshots

The images/ folder includes the full breakdown:

asg1–asg3 → Launch Template creation

asg4–asg9 → ASG setup screens

asg10–asg12 → Scaling configuration

asg13–asg15 → Instance replacement in action

These provide a clear visual walkthrough for anyone following the project.

🧠 Why This Matters

This small project demonstrates real infrastructure automation principles:

High availability

Self-healing systems

Infrastructure as code (conceptually)

Horizontal scaling fundamentals

It’s beginner-friendly but covers key real-world AWS concepts.

✔️ Status

Completed — All screenshots included, ASG tested, README documented.
