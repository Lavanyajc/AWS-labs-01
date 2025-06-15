
## 🎥 Demo Video

▶️ [Click here to watch the video demo](https://drive.google.com/file/d/1f1hEo_-2643ZNsvw1YlUj2i_E53OLasj/view?usp=sharing)


# 🛡️ IAM Lab: Attach and Detach Policies to IAM Users

## 📌 Objective
Learn how to attach and detach IAM policies to users using the AWS Console and AWS CLI.

---

## 🧪 Lab Steps

### 👤 1. Create an IAM User
- Go to AWS IAM Console → **Users** → **Add user**
- Name: `test-user`
- Select **Programmatic access**
- Click **Next** → Skip group → Click **Next** → Create user

---

### 📎 2. Attach a Policy (AWS Console)
- Go to `test-user` → **Permissions** tab → **Add permissions**
- Choose **Attach policies directly**
- Select `AmazonS3ReadOnlyAccess`
- Click **Next** → Add → Done ✅

---

### 💻 3. Attach Policy via CLI
```bash
aws iam attach-user-policy \
  --user-name test-user \
  --policy-arn arn:aws:iam::aws:policy/AmazonEC2ReadOnlyAccess
````

⏺️ This gives EC2 read access to `test-user`

---

### 🚫 4. Detach Policy via CLI

```bash
aws iam detach-user-policy \
  --user-name test-user \
  --policy-arn arn:aws:iam::aws:policy/AmazonEC2ReadOnlyAccess
```

🧹 This removes the EC2 read access policy from the user

---

## 📄 Verify Attached Policies (Optional)

```bash
aws iam list-attached-user-policies --user-name test-user
```

---

## 🧼 5. Cleanup (Optional)

```bash
aws iam delete-user --user-name test-user
```

---



## ✅ Output Verification

You can test the permissions by:

* Logging in as `test-user`
* Trying to access S3 and EC2 via AWS CLI

---

## 📚 Concepts Covered

* IAM Policies
* IAM Users
* Attach/Detach Permissions
* AWS CLI Practice

---



