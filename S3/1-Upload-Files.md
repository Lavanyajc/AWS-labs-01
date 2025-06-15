 
## 🧪 S3 Lab: Upload Files using AWS CLI

### ✅ Objective:
Upload a local file to an S3 bucket using the AWS CLI with correct IAM permissions.



### 🛠️ Steps Performed:

1. **Created an S3 bucket**  
   - Bucket name: `jc11` (globally unique)
   - Used AWS Console → S3 → Create Bucket  
   - Chose default settings for ACLs and public access block.

2. **Created a test file locally**  
   ```bash
   echo "hello,aws!" > testfile.txt
   ```

3. **Configured the IAM User**  
   - Created an IAM user with `AmazonS3FullAccess` policy (or a custom policy for upload only).
   - Configured credentials on CLI:
     ```bash
     aws configure
     ```
   - Entered Access Key, Secret Key, Region (`ap-south-1`), and output format (`json`).

4. **Uploaded the file using CLI**  
   ```bash
   aws s3 cp testfile.txt s3://jc11/
   ```

5. **Verified the upload**  
   - Logged into AWS Console → S3 → `jc11` bucket
   - Confirmed `testfile.txt` is present.

---

### 🔐 IAM Policy Used (for full access):
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:*",
      "Resource": "*"
    }
  ]
}
```

---

### ✅ Outcome:
File was successfully uploaded from local machine to the specified S3 bucket via AWS CLI.

