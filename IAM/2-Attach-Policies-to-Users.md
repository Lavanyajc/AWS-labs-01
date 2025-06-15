 # IAM Lab 2: Attaching Policies to IAM Users
## 🎥 Demo Video

▶️ [Click here to watch the video demo](https://drive.google.com/file/d/1f1hEo_-2643ZNsvw1YlUj2i_E53OLasj/view?usp=sharing)

## ✅ Tasks Performed:

### 1. Created IAM User: `practice-user`
- Created through Console
- Verified user using CLI

### 2. Attached AWS Managed Policy `AmazonEC2ReadOnlyAccess`
aws iam attach-user-policy --user-name practice-user --policy-arn arn:aws:iam::aws:policy/AmazonEC2ReadOnlyAccess

### 3. Verified Permissions:
aws sts get-caller-identity  
aws ec2 describe-instances  # ✅ Worked because user had read-only access

### 4. Detached Policy:
aws iam detach-user-policy --user-name practice-user --policy-arn arn:aws:iam::aws:policy/AmazonEC2ReadOnlyAccess

### 5. Rechecked access:
aws ec2 describe-instances  # ❌ Access Denied (as expected)

---

Outcome:
- Understood how IAM policies affect user permissions.
- Successfully attached/detached policies and validated their impact via CLI.
