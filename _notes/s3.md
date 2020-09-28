---
title: AmazonS3
---

[[AWS]] Simple Storage Service

## Making folders publicly readable in an Amazon S3 bucket
Give public read (get) access to certain folders.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your.bucket.name/uploads/*"
        },
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your.bucket.name/video/*"
        }
    ]
}
```