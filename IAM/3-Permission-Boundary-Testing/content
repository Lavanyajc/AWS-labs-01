Great! If you're focusing on **console-only steps**, here’s the corrected and simplified version of **IAM Lab 3 (Permissions Boundary)** with **console-based instructions only**:

---

# ✅ IAM Lab 3: Set Permissions Boundary for IAM User (Console Only)

---

## 🔧 Tasks Performed:

### 1. **Create a Custom Permissions Boundary Policy**

- Go to **IAM > Policies > Create policy**
- Choose **JSON** tab and paste:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowEC2ActionsOnly",
      "Effect": "Allow",
      "Action": "ec2:*",
      "Resource": "*"
    }
  ]
}
```

- Click **Next**, then **Name** it: `IAM-Boundary-EC2`
- Create the policy

---

### 2. **Attach the Permissions Boundary to `practice-user`**

- Go to **IAM > Users > practice-user**
- Click **Permissions** tab → Scroll down to **Permissions boundary**
- Click **Add permissions boundary**
- Select the policy `IAM-Boundary-EC2` → Click **Next → Add boundary**

---

### 3. **Verify Boundary Is Attached**

- Still on the `practice-user` page, under **Permissions boundary**, you should see:

> ✅ IAM-Boundary-EC2 (Permissions boundary ARN listed)

---

## 4. 🔍 **Test the Permissions (Using Console or cli)**

- Go to **EC2 Console → Instances**
  - Try to view EC2 instances — ✅ It should work.
  
- Go to **IAM Console → Users**
  - Try to list or manage users — ❌ Should show **Access Denied** or blank list.



## 🔍 **Testing Permissions via CLI**

### ✅ Action allowed by boundary:
```bash
aws ec2 describe-instances
```
> ✅ **Expected Output:** Works successfully (because `ec2:*` is allowed by the boundary).

---

### ❌ Action blocked by boundary:
```bash
aws iam list-users
```
> ❌ **Expected Output:**  
```json
An error occurred (AccessDenied) when calling the ListUsers operation: User is not authorized to perform: iam:ListUsers
```
> Because `iam:*` is **not included** in the boundary, even if user policy allows it.

---



---

### 5. **Remove the Permissions Boundary**

- Back in **IAM > Users > practice-user > Permissions**
- Click **Remove** next to **Permissions boundary**
- Confirm removal

---

## 🧠 Outcome:

- Understood how **Permissions Boundaries limit IAM users**, even when other permissions are allowed.
- Saw clear distinction between:
  - **Policies** (grant permissions)
  - **Boundaries** (restrict maximum permissions)


