---
title: "Prerequisites"
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

### IAM Permissions

Attach AdministratorAccess in the IAM permission policy to your AWS account for easier workflow.

**Note:** Using Administrator privileges is only recommended for Workshop environments to ensure uninterrupted deployment. In a real-world Production environment, Least Privilege principles must be followed for each service.

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "*",
            "Resource": "*"
        }
    ]
}
```

#### Source Code
Repository GitHub chứa code .NET Core và Dockerfile hợp lệ
