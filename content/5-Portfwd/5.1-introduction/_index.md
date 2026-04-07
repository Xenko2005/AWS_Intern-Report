---
title: "Introduction"
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

### Introduction to AnTiScaQ (Anti-Scam Alert Platform)

**AnTiScaQ** is a modern, **automated anti-scam alert platform** designed to protect users from increasingly sophisticated cybersecurity threats. At its core lies the power of **open-source data intelligence**, utilizing robust scraping engines to deep-dive analyze and verify the risk levels of suspicious **phone numbers, email contents, and domains**. The groundbreaking differentiator of AnTiScaQ is its ability to provide **real-time risk scoring**, enabling the immediate detection, evaluation, and issuance of alerts the moment phishing campaigns break out. This continuous process enriches the threat intelligence database, maximizing safety for users and the community.

### AWS Solution Architecture Overview

![Networking Session](/AWS_Intern-Report/images/aws_architecture.drawio.png)

**Solution Architecture:**

The **AnTiScaQ** ecosystem is built upon a **Serverless** architecture model, comprehensively leveraging the elite services of the **AWS** cloud platform to deliver highly elastic scalability and **drastically minimize operational costs**. Strictly adhering to the core pillars of the **AWS Well-Architected Framework**, this solution ensures the system remains resilient, secure, and ready to instantly handle massive traffic surges during sudden phishing outbreaks.

* **Compute & Logic Layer**
At the heart of the processing layer, the platform utilizes the combined power of **Amazon API Gateway** and **AWS Lambda** as its primary compute engine, operating **entirely without server management**. Within this architecture, compute functions shoulder the responsibility of processing high-speed REST API queries against the threat database, while specialized Python functions seamlessly execute asynchronous open-source data scraping workflows.

* **Data & Persistence Layer**
To solve the challenge of real-time retrieval performance, the system relies on **Amazon DynamoDB** as its central NoSQL database, applying single-table design techniques to store threat intelligence profiles with sub-second latency. Accompanying the database layer is **Amazon S3**, configured as a secure repository for unstructured data such as forensic image evidence, while simultaneously acting as the host for all static assets of the web portal interface.

* **Security & Authentication**
To establish a formidable defense perimeter, the architecture deeply integrates **Amazon Cognito** for identity management, supporting highly granular authentication and Role-Based Access Control (RBAC). Alongside this, **AWS Secrets Manager** serves as a secure vault to automatically store and rotate sensitive information like database credentials and API tokens. Meanwhile, the **AWS WAF** firewall operates on the frontline to shield API endpoints from botnet abuse and Distributed Denial of Service (DDoS) attacks.

* **DevOps & Monitoring**
To maintain the pace of feature releases and ensure quality, the entire build and deployment lifecycle (CI/CD) is fully automated end-to-end via **GitHub Actions**. On the network delivery front, **Amazon CloudFront** CDN is deployed in tandem with **Amazon S3** to deliver the web interface content at maximum speed to global users. Finally, every system state—from API rate limits to scraping processes—is closely monitored by the duo of **Amazon CloudWatch** and **Amazon SNS**, automatically triggering instant alert workflows upon detecting errors or anomalous cost thresholds.


