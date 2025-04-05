# S3 Labs – Amazon Simple Storage Service

This section includes labs demonstrating file storage, access control, and IAM integration with S3 using AWS Console and CLI.

## Labs Completed

1. Upload Files to S3 Bucket  
   - Created S3 bucket using AWS Console  
   - Uploaded test files via Console  
   - Verified uploads using `aws s3 ls` and `aws s3 cp` commands  

2. Download Files via CLI  
   - Used `aws s3 cp s3://<bucket-name>/file.txt file_downloaded.txt`  
   - Verified content of the downloaded file  

3. Access S3 with IAM User  
   - Created IAM user with custom S3 access policy  
   - Attached inline policy allowing only specific bucket actions  
   - Tested access through AWS CLI and verified permission behavior  

## Best Practices Used

- Bucket names followed global uniqueness and naming conventions  
- Applied least privilege to IAM users accessing S3  
- Verified access control via CLI for robust testing  
- Avoided using root credentials for S3 operations  
- Used IAM policies to explicitly allow and deny actions where necessary  
