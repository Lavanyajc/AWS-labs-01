
✅ EC2 Lab 4: Block EC2 Access Using Deny Policy

🔹 Objective:
To explicitly deny EC2 actions for a specific IAM user using an inline "Deny" policy.

🔹 Steps Performed:

1️⃣ Created an IAM user (e.g., `blockuser`) via AWS Console.

2️⃣ Attached a policy that grants EC2 access (optional):
   - AWS-managed policy like `AmazonEC2ReadOnlyAccess`

3️⃣ Created and attached a custom inline Deny policy:
   - Denied all EC2 actions explicitly

   JSON Policy:
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

4️⃣ Switched to the `blockuser` IAM user via Console.

5️⃣ Tried accessing EC2 Dashboard or performing EC2 actions:
   - Result: Access Denied (Explicit Deny overrides any Allow)

6️⃣ Verified Deny effect using AWS CLI as the `blockuser`:
   ```
   aws ec2 describe-instances
   ```
   - Output: Error message indicating lack of permission due to Deny policy

📝 Notes:
- Explicit Deny always overrides any Allow policies.
- Used inline policy under IAM user -> Permissions tab.

✔️ Outcome:
Successfully demonstrated how to block EC2 access for an IAM user using Deny policies.
```


