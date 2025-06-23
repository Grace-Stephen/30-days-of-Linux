# 🚀 Day 22: Log Rotation, Network Monitoring, and Bash Scripting Basics

## 🎯 Overview

Today's session builds upon the automation and networking tasks from Day 21 by introducing:

- **Log rotation** for managing growing files
- **Network uptime monitoring** using ping
- **Basic Bash scripting** with user interaction (`echo`, `read`, variables`)

---

## ✅ Tasks Completed

### 🗂️ 1. Verified Cron Job Output
Viewed the live content of `time_log.txt` to confirm the cron job from Day 21 was still running and logging time. 

### 📏 2. Checked File Size of `time_log.txt`
Used the `stat` command to check the exact size of the log file in bytes and determine if rotation was necessary.

### 🔍 3. Verified `gzip` Was Installed
Confirmed that `gzip` (used for compressing logs) was available.

### 🔁 4. Wrote a Log Rotation Script
Created a script to check log size, archive it with a timestamp, compress it with `gzip`, and recreate a new log file.

### 🧾 5. Made Rotation Script Executable and Scheduled It
Used `chmod +x` and `crontab -e` to schedule it every 5 minutes.

### 🌐 6. Created Network Uptime Monitoring Script
Script logs either "Network is UP" or "Network is DOWN" using a ping test.

### 🔒 7. Made Network Script Executable
Confirmed that the script runs manually and logs status to `uptime_log.txt`.

### 🕑 8. Scheduled the Network Script via Cron
Configured the network check script to run every 2 minutes.

### 📦 9. Confirmed Time Log Rotation Worked
Verified that:
- The log file rotated after reaching a threshold
- `.gz` archive was created with a timestamp
- A fresh log file was started

### 📡 10. Confirmed Network Script Was Running
Checked the output file to confirm timestamped status messages were being recorded every 2 minutes.

### 👤 11. Created a User-Prompting Script
Practiced using `echo`, `read`, and Bash variables for interactive shell scripts.

### 🏁 12. Made Script Executable and Ran It
Ran the script manually in the terminal and confirmed the user interaction worked as expected.

---

## 📸 Screenshot Gallery: all in the images folder

1. ✅ Viewed the output of the time log cron job set in Day 21  
2. 📏 Checked the current file size of the time log  
3. 🔍 Confirmed `gzip` is installed on the system  
4. 📝 Created a rotation script for the time log  
5. 🛠️ Made the script executable and added a cron job  
6. 🌐 Created a script to monitor network status  
7. 🔒 Made the network script executable  
8. 🕒 Scheduled the rotation script to run every two minutes  
9. 📦 Confirmed the time log file rotated successfully  
10. 📡 Verified that the network status script is running  
11. 👤 Created a user-prompting Bash script  
12. ✅ Made the user script executable and ran it manually

---

## 🧠 Key Concepts Practiced

| Concept | Skills Applied |
|--------|----------------|
| Bash Scripting | `echo`, `read`, variables, shebang |
| File Handling | Checking file size, rotating and compressing logs |
| Cron Jobs | Scheduling and testing background scripts |
| Network Diagnostics | Using `ping` and scripting uptime checks |
| Permissions | `chmod +x` to make scripts executable |
