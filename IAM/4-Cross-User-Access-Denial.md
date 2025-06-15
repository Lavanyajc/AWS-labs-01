

### 📁 Lab: Cross-User Access Denial (UserA Denied Access to jc's S3 Bucket)

####  Steps Performed:

1. **Created 2 IAM Users**:  
   - `UserA`  
   - `jc`  

2. **Created an S3 Bucket**:  
   - Bucket name: `jc11`  
   - Created by user `jc`

3. **Uploaded a File to S3 Bucket**:  
   - File: `testfile.txt` with content: `"hello, aws!"`  
   - Uploaded via `jc` account

4. **Tested Cross-Access by Switching to UserA**:
   - Used CLI with `UserA` credentials  
   - Ran command:  
     ```bash
     aws s3 cp s3://jc11/testfile.txt testfile_downloaded.txt
     ```
   - ✅ Got **Access Denied** (expected)

5. **Why Access Denied?**  
   - No S3 bucket policy allowed UserA  
   - IAM policy did not permit UserA to access `jc11`

6. 
   - By default, **S3 buckets are private**, and IAM users can't access each other's resources unless explicitly granted.




### ✅ Steps to **Allow Cross-User Access** to S3 Bucket:

#### 1. **Created a Bucket Policy on `jc11` Bucket**  
You modified the **S3 bucket policy** (as `jc` or root user) to allow `UserA` to access the bucket:

📄 **Bucket Policy JSON**:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowUserAReadAccess",
      "Effect": "Allow",
      "Principal": {
        "AWS": "arn:aws:iam::522814729380:user/UserA"
      },
      "Action": [
        "s3:GetObject"
      ],
      "Resource": "arn:aws:s3:::jc11/*"
    }
  ]
}
```

This policy allowed `UserA` to download (read) objects from `jc11`.

---

#### 2. **Switched to `UserA` Again**

✅ You ran the same command again:
```bash
aws s3 cp s3://jc11/testfile.txt testfile_downloaded.txt
```

success now.. 
You used `type testfile_downloaded.txt` and saw the output:
```
hello, aws!
```

-



