## 🎥 Demo Video

▶️ [Click here to watch the video demo](https://drive.google.com/file/d/17hjWidu8j1oWCtn84r93TaDMNzaR7yJY/view?usp=sharing)

# S3 Storage Classes Hands-On

## Steps:
1. Upload an object and choose storage class:
   - Standard
   - Infrequent Access (IA)
   - Intelligent Tiering
   - Glacier (for archival)

2. Enable Lifecycle Rule:
   - Bucket → Management → Lifecycle Rule → Create
   - Transition from Standard → IA after 30 days → Glacier after 90 days

3. Observe object transition over time (or simulate using CLI)


