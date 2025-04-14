# ✅ Create and Attach EBS Volume using AWS Console

## 🔸 Objective:
Create an Elastic Block Store (EBS) volume and attach it to an existing EC2 instance to provide persistent storage.

---

## 🛠️ Steps to Create EBS Volume:

1. **Go to EC2 Dashboard**:
   - Navigate to **Elastic Block Store → Volumes**

2. Click **Create Volume**

3. Enter the following:
   - **Volume Type**: gp3 (general purpose)
   - **Size**: e.g., 8 GiB
   - **Availability Zone**: Must match your EC2 instance's AZ (e.g., `us-east-1a`)
   - Optionally set:
     - **Encryption**
     - **Tags** (e.g., Name: MyDataVolume)

4. Click **Create Volume**

---

## 🔗 Steps to Attach Volume to EC2:

1. In **Volumes**, select your created volume.

2. Click **Actions → Attach Volume**

3. Choose:
   - **Instance ID**: Select your running instance
   - **Device Name**: Use default or set (e.g., `/dev/xvdf`)

4. Click **Attach**

---

## 🔍 Check in EC2:
- Go to **EC2 → Instances → Select instance**
- Scroll to **Storage** section to see attached volume(s)

---

## 💡 Real-World Use Case Scenarios:

### 1. 💽 Additional Storage for Applications
- Use an EBS volume to store large datasets, logs, or media files outside the root volume.

### 2. 🛠️ Separate Volume for Databases
- Keep database data on a separate EBS volume (e.g., `/dev/xvdf`) for easier backup and scaling.

### 3. ♻️ Reuse Volume Across Instances
- Detach from one EC2 and attach to another to move data without copying over the network.

### 4. 🔐 Encrypted Data Storage
- Create encrypted EBS volumes to store sensitive information securely.

### 5. 📂 Backup Strategy
- Create volumes just for backup scripts or snapshots of critical data.

---

## 📝 Tip:
- You must **mount** and **format** the volume from within the EC2 instance using SSH:
  ```bash
  sudo mkfs -t ext4 /dev/xvdf
  sudo mkdir /data
  sudo mount /dev/xvdf /data

##Add to /etc/fstab for auto-mount on reboot.
