//do not attach policies unless it needed in project, especially do not give administrator access everytime okiee dude!
```
✅ EC2 Lab 5: Test EC2 Access With IAM Permissions

🔹 Objective:
To test EC2 access for different IAM users based on attached IAM policies (Allow/Deny).

🔹 Steps Performed:

1️⃣ Created two IAM users:
   - `UserAllow` → To allow EC2 actions
   - `UserDeny` → To restrict EC2 actions

2️⃣ Attached permissions:
   - `UserAllow`: Attached `AmazonEC2ReadOnlyAccess`
   - `UserDeny`: Attached custom **Deny** inline policy:
     ```json
     {
       "Version": "2012-10-17",
       "Statement": [
         {
           "Effect": "Deny",
           "Action": "ec2:*",
           "Resource": "*"
         }
       ]
     }
     ```

3️⃣ Generated Access Key and Secret for both users via Console:
   - Used for configuring AWS CLI:
     ```
     aws configure
     ```

4️⃣ Switched between IAM users in CLI and ran:
   ```
   aws ec2 describe-instances
   ```

5️⃣ Observations:
   - `UserAllow`: Successfully listed instances (permission granted)
   - `UserDeny`: Access denied due to explicit Deny policy

📝 Notes:
- Deny policies override any Allow permissions.
- Verified the practical effect of IAM permissions through CLI testing.

✔️ Outcome:
Successfully validated how IAM policies control EC2 access in real-time using AWS CLI.
```

