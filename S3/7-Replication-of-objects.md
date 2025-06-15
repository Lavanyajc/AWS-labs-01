# S3 Cross-Region Replication (CRR)
## 🎥 Demo Video

▶️ [Click here to watch the video demo](https://drive.google.com/file/d/12-BtJ9qy49-2HPcjcLEAroe7x4oIXfbm/view?usp=sharing)

## Steps:
1. Create two buckets in different regions:
   - Source: `jc-source-bucket` (Mumbai)
   - Destination: `jc-dest-bucket` (Singapore)

2. Enable Versioning on both buckets

3. Go to source bucket → Management → Replication Rules → Create rule

4. Rule Settings:
   - Apply to all objects
   - Destination bucket: Choose destination ARN
   - IAM role: Create new role

5. Upload a file to source → Wait → Check destination

✅ File is replicated across regions!
