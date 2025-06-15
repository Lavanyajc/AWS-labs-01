# IAM Lab 1: Creating Users and Groups

## ✅ Tasks Performed:

### 1. Created a new IAM user named `jc`
- Through AWS Console
- Enabled programmatic access and/or console access
- Attached policies directly or via group

### 2. Created a new IAM group named `demo`
- Used AWS Console and CLI

### 3. Added the user `jc` to the `demo` group
- Verified group membership

---

## 💻 AWS CLI Commands Used: // here you can create users,groups,attach/remove policies using console itself cli optional

# Create IAM user
aws iam create-user --user-name jc

# Create IAM group
aws iam create-group --group-name demo

# Add user to group
aws iam add-user-to-group --user-name jc --group-name demo

# Verify user is added to group                //here we use  cli mainly for verification 
aws iam get-group --group-name demo

# List all IAM users
aws iam list-users

# List all IAM groups
aws iam list-groups

---

 Outcome:
- Successfully created and grouped IAM users via Console and CLI.
- Verified user-group relationships using `get-group` command.
 
