
✅ EC2 Lab 3: Describe EC2 Instances via CLI

🔹 Objective:
To use AWS CLI to retrieve information about EC2 instances in the current region.

🔹 Steps Performed:

1️⃣ Opened Command Prompt and Configured CLI (if not already):
   ```
   aws configure
   ```
   - Provided Access Key, Secret Key, Region (e.g., ap-south-1), and output format (json or table)

2️⃣ Used describe-instances command:
   ```
   aws ec2 describe-instances
   ```

3️⃣ Filtered output using query for clarity:
   Example - Display instance IDs:
   ```
   aws ec2 describe-instances --query "Reservations[*].Instances[*].InstanceId" --output table
   ```

   Example - Display public IPs:
   ```
   aws ec2 describe-instances --query "Reservations[*].Instances[*].PublicIpAddress" --output table
   ```

4️⃣ Verified instance details:
   - Instance ID
   - Public IP
   - Instance type
   - Availability Zone
   - IAM Role (if attached)
   - State (running/stopped)

📝 Notes:
- Ensured AWS CLI was installed (`aws --version`)
- Ran commands from Windows CMD or Terminal

✔️ Outcome:
Successfully retrieved and filtered EC2 instance metadata using AWS CLI.


