✅ EC2 Lab 1: Create and Connect to EC2 Instance (Console + CLI)

🔹 Objective:
To launch an EC2 instance using the AWS Console and connect to it using the AWS CLI and SSH (without using MobaXterm).

🔹 Steps Performed:

1️⃣ Created EC2 instance:
   - Chose Amazon Linux 2 AMI
   - Instance type: t2.micro (Free tier)
   - Created and downloaded a new key pair named `jc-key.pem`
   - Allowed SSH (port 22) in security group settings
   - Launched instance successfully

2️⃣ Connected to EC2 using SSH from CMD:
   - Navigated to the directory containing the `jc-key.pem` file
   - Ran the command:
     ```
     ssh -i "jc-key.pem" ec2-user@<Public-IP-of-instance>
     ```
   - Accepted the fingerprint prompt
   - Successfully accessed the EC2 instance shell

3️⃣ Validated EC2 connection:
   - Ran:
     ```
     hostname
     uname -a
     ```
   - Confirmed we were inside the EC2 instance

📝 Notes:
- The EC2 instance must be in running state
- Security group must allow inbound SSH from your IP
- If on Windows, use Git Bash or WSL for SSH if CMD has issues

✔️ Outcome:
Successfully launched and connected to EC2 using AWS Console + CLI (ssh).
