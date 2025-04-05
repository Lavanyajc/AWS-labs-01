 

## 🧪 S3 Lab: Download Files using AWS CLI

### ✅ Objective:
Download a file from an S3 bucket to the local system using the AWS CLI with correct IAM permissions.

---

### 🛠️ Steps Performed:

1. **Verified the file exists in the bucket**
   - File `testfile.txt` was already uploaded to the S3 bucket `jc11`.

2. **Used AWS CLI to download the file**
   ```bash
   aws s3 cp s3://jc11/testfile.txt testfile_downloaded.txt  //this 2 commands are enough here
   ```

3. **Checked file contents locally**
   - Since `cat` doesn’t work on Windows CMD, used:
     ```bash
     type testfile_downloaded.txt
     ```
   - Output:
     ```
     hello,aws!
     ```

---

### 🔐 IAM Policy Used (for download):     //use if policy is not given
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["s3:GetObject"],
      "Resource": "arn:aws:s3:::jc11/*"
    }
  ]
}
```

---

### ✅ Outcome:
File `testfile.txt` was successfully downloaded from the S3 bucket `jc11` to the local system using AWS CLI.

