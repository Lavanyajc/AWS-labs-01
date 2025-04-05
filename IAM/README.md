### 📁 IAM Labs – AWS Identity and Access Management

This folder contains hands-on labs and mini-projects on AWS IAM. Each lab demonstrates key IAM concepts using AWS Console and CLI.

---

### ✅ Labs Covered

1. **Create Users and Groups**  
   Created multiple IAM users, organized them into groups, and attached AWS managed policies for permission control.

2. **Attach Policies to Users**  
   Explored attaching custom and managed policies to users to grant or restrict specific permissions.

3. **Permission Boundaries**  
   Implemented permission boundaries using JSON policies to control the maximum allowed permissions for users.

4. **Cross-user Access Restriction**  
   Tested scenarios where one IAM user was restricted from accessing resources belonging to another IAM user using deny policies.

5. **Attach & Detach IAM Policies**  
   Attached policies to users to allow specific actions, then detached them to test access revocation via CLI.

6. **Check Access with CLI**  
   Used AWS CLI commands (`aws iam list-users`, `aws s3 cp`) to test permissions before and after policy application.

7. **MFA Setup for IAM User**  
   Enabled Multi-Factor Authentication (MFA) using virtual MFA device for a user and verified its working by CLI.

---

### 📌 Best Practices Followed

- Followed **least privilege principle**: Only necessary permissions were granted to each user.
- Implemented **permission boundaries** to define permission caps.
- Tested policies using **CLI for validation**.
- **MFA was enforced** to enhance IAM user security.
- **Custom deny policies** were tested for cross-user isolation.

---

### 🛠️ Tools Used

- **AWS Console** for creating users, groups, policies
- **AWS CLI** for verifying access permissions and testing scenarios
