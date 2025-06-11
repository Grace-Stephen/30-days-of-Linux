# 📅 Day 14 – User Management & Background Processes
Today’s challenge covered:
- Creating users and groups
- Managing directory permissions
- Running and controlling background processes

---

## 🧪 Real-World Scenario

You're onboarding a new developer, assigning them access to a shared directory, and teaching them how to manage/monitor system activity.

---

## ✅ Tasks Completed

### 1️⃣ Created a User and Group
- Created a new user and group
- Added the user to the group

```bash
sudo adduser monitor_jane
sudo groupadd monitors
sudo usermod -aG monitors monitor_jane

2️⃣ Created a Shared Directory and changed ownership/permissions to allow group access

sudo mkdir /var/syscheck
sudo chown monitor_jane:monitors /var/syscheck
sudo chmod 770 /var/syscheck

3️⃣ Signed in as the New User

sudo su - monitor_jane

4️⃣ Ran a System Monitoring Command in the Background
- Used nohup and top to run system monitoring
- Saved output to a file inside the shared directory
command:
sudo nohup top -b -n 30 > /var/syscheck/top_log.txt &

5️⃣ Pinged Google in the Background and Logged Output

nohup ping google.com > /var/syscheck/ping_log.txt &

6️⃣ Checked and Managed Background Jobs
jobs             # View background jobs
fg %1            # Bring a job to the foreground
bg %1            # Resume job in background

7️⃣ Monitored System Status and Killed a Job

top              # Checked live system usage
free -h          # Viewed memory and swap space
kill %1          # Stopped a background job

📸 Screenshots Preview
Screenshots for each task are included in the image folder for Day 14.

💡 What I Learned
How to properly set up a shared directory and assign group access

How to use nohup, jobs, fg, bg, and kill

How to handle permission errors and background command logging