# EC2 Labs – Amazon Elastic Compute Cloud

This section includes hands-on labs demonstrating how to manage EC2 instances and IAM integrations using AWS Console and CLI.


## Labs Completed

1. Create and Connect to EC2 Instance  
   - Launched EC2 instance via Console  
   - Downloaded and used key pair  
   - Connected using AWS CLI  

2. Attach IAM Role to EC2  
   - Created IAM Role with AmazonS3ReadOnlyAccess  
   - Attached role to EC2 instance via Console  
   - Verified access by listing S3 buckets from the instance  

3. Describe Instances via CLI  
   - Used `aws ec2 describe-instances` to get instance metadata  

4. Block EC2 Access using Deny Policy  
   - Created and attached a custom inline Deny policy  
   - Restricted stop/terminate actions for specific users  

5. Test EC2 Access with IAM User  
   - Created IAM user with limited EC2 permissions  
   - Tested access by running EC2 commands through CLI  

## Best Practices Used

- Used IAM roles instead of access keys  
- Applied principle of least privilege  
- Tested all permissions through AWS CLI  
- Created clear boundaries using explicit Deny policies  
- Followed secure connection methods for EC2 access  
