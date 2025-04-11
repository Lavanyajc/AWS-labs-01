
✅ Lab: Configure and Test MFA (Multi-Factor Authentication)

🔸 Goal:
Enable MFA for an IAM user and test CLI behavior with and without MFA.

✅ Steps Performed:

1. Created IAM User (UserMFA)
- Created via AWS Console with programmatic access.
- Downloaded access and secret keys.
- No MFA initially enabled.

2. Tested CLI Access Before Enabling MFA
- Configured AWS CLI using:
  aws configure
- Verified access with:
  aws s3 ls
- ✅ Output: Successfully listed S3 buckets (no MFA restrictions yet).

3. Enabled Virtual MFA
- Went to IAM → UserMFA → Security Credentials tab.
- Assigned virtual MFA using Google Authenticator.
- Scanned QR code and entered two consecutive OTPs.

4. Created and Attached Policy to Enforce MFA
- Created custom IAM policy named `DenyWithoutMFA`:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "BlockActionsWithoutMFA",
      "Effect": "Deny",
      "Action": "*",
      "Resource": "*",
      "Condition": {
        "BoolIfExists": {
          "aws:MultiFactorAuthPresent": "false"
        }
      }
    }
  ]
}
```
- Attached this policy to UserMFA via the AWS Console.

5. Tested CLI Access After Enabling MFA
- Ran:
  aws s3 ls
- ❌ Result: Access denied as MFA is required and not passed in CLI.

6. Console Login Test
- Logged into AWS Console as UserMFA.
- Prompted for and entered MFA code from Google Authenticator.
- ✅ Successful login.

🎯 Outcome:
MFA was enforced via IAM policy and tested from both AWS Console and AWS CLI. Verified that CLI actions were denied when MFA was not present.
```


