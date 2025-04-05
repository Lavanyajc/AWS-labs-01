
## 🧪 S3 Lab: Access S3 with IAM User

### ✅ Objective:
Access S3 buckets using an IAM user with limited permissions and verify access via AWS CLI.

---

### 🛠️ Steps Performed:

1. **Created an IAM user**  
   - Name: `s3user`
   - Programmatic access enabled
   - Saved Access key ID and Secret

2. **Attached a custom policy to allow limited S3 access**
   - Allowed only read access (List and GetObject)

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["s3:ListBucket", "s3:GetObject"],
      "Resource": [
        "arn:aws:s3:::jc11",
        "arn:aws:s3:::jc11/*"
      ]
    }
  ]
}
```

3. **Configured AWS CLI with IAM credentials**
   ```bash
   aws configure
   ```
   - Entered IAM user's credentials  
   - Verified region and output format

4. **Tested access with CLI**
   - Listed the bucket:
     ```bash
     aws s3 ls
     ```
   - Listed files inside the bucket:
     ```bash
     aws s3 ls s3://jc11
     ```
   - Downloaded a file:
     ```bash
     aws s3 cp s3://jc11/testfile.txt testfile_downloaded.txt
     ```

---

### ❌ Denied Upload Access:
   - Tried uploading a file (without permission):
     ```bash
     aws s3 cp testfile.txt s3://jc11/
     ```
   - Resulted in **AccessDenied**, as expected.

---

### ✅ Outcome:
Successfully accessed and downloaded files from S3 using an IAM user with restricted permissions. Verified that upload (write) access was denied due to policy.

```

