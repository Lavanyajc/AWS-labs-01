## 🎥 Demo Video

▶️ [Click here to watch the video demo](https://drive.google.com/file/d/1txBS8fdBc3eRyMCVNOWMJAeoBhzBLFn0/view?usp=sharing)

```

## ✅ - S3 Static Website Hosting (Hands-On)

```md
# S3 Static Website Hosting

## Steps:
1. Go to S3 → Create Bucket (e.g., `jc-static-site`)
   - Enable public access
   - Disable Block Public Access settings

2. Upload files:
   - Upload `index.html` and `error.html`

3. Enable Static Website Hosting:
   - Go to bucket → Properties tab → Static Website Hosting → Enable
   - Index document: `index.html`
   - Error document: `error.html`

4. Permissions:
   - Add bucket policy to allow public read access

```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Sid": "PublicReadWebsite",
    "Effect": "Allow",
    "Principal": "*",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::jc-static-site/*"
  }]
}



---

## ✅ 136 - S3 Versioning Hands-On

```md
# S3 Versioning Hands-On

## Steps:
1. Go to bucket → Properties → Enable Versioning

2. Upload a file `version.txt`

3. Upload `version.txt` again with different content

4. Go to "Versions" tab → View all versions of the file

5. Download or delete specific versions

6. Optional: Suspend versioning and test behavior
