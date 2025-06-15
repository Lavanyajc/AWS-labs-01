# S3 Bucket Policy Hands-On

## Objective: Make bucket or object public using Bucket Policy

## Steps:
1. Go to S3 Console → Select your bucket
2. Permissions tab → Edit Bucket Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Sid": "PublicReadGetObject",
    "Effect": "Allow",
    "Principal": "*",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::jc-s3-bucket-name/*"
  }]
}

## 🎥 Project Demo

👉 [Click here to watch the demo video](https://drive.google.com/file/d/1JPwZ9Z5G7MG02vqREbII8CWD99W7sx_H/view?usp=sharing)
