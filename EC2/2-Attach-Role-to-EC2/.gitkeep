 ✅ EC2 Lab 2: Attach IAM Role to EC2 Instance

🔹 Objective:
To attach an IAM role to an EC2 instance to grant it permissions (e.g., to access S3) without using access keys.

🔹 Steps Performed:

1️⃣ Created IAM Role:
   - Service: EC2
   - Attached policy: AmazonS3ReadOnlyAccess
   - Named the role: `EC2-S3ReadOnly-Role`
   - Successfully created the role

2️⃣ Attached Role to Running EC2 Instance:
   - Navigated to EC2 > Instances > Actions > Security > Modify IAM Role
   - Selected `EC2-S3ReadOnly-Role` and applied changes

3️⃣ Verified Role Permissions on EC2 via CLI:
   - SSH'd into the EC2 instance using:
     ```
     ssh -i "jc-key.pem" ec2-user@<Public-IP>
     ```
   - Ran command to list S3 buckets:
     ```
     aws s3 ls
     ```
   - Output showed accessible S3 buckets (read-only access)

📝 Notes:
- No access keys were configured inside the instance
- Instance profile was automatically updated after attaching the role
- Confirmed the role worked through metadata:


✔️ Outcome:
Successfully attached an IAM role to EC2 and accessed S3 via CLI without using user credentials.


