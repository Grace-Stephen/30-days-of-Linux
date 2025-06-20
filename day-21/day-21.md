# 📅 Day 21: Automating Tasks with Cron + Network Diagnostics

## 🎯 Goal
Practice real-world Linux system administration tasks by:
- Automating a log-writing task using `cron`
- Verifying and troubleshooting network configuration and connectivity

---

## ✅ Tasks Completed

### 📝 1. Created a Script to Log Time
- Created a `scripts/` directory inside `~/admin-project`

- Wrote a shell script to append the current date and time to a log file every minute:

```bash
#!/bin/bash
echo "$(date)" >> ~/admin-project/logs/time_log.txt

🔐 2. Made Script Executable

chmod +x ~/admin-project/scripts/log_time.sh

⏱️ 3. Scheduled Cron Job to Run Every Minute
Used crontab -e to schedule the job:

* * * * * ~/admin-project/scripts/log_time.sh
This runs the script every minute to simulate time-based automation.

🔍 4. Verified Cron Job is Running
After a few minutes, confirmed that the time_log.txt file was being updated every minute with new timestamps.

🌐 Network Diagnostics
📡 5. Checked IP Configuration and Routing Table
Used:

ip a
ip route
This showed active interfaces, assigned IP addresses, and the default route.

🔄 6. Verified Network Connectivity
Used:
ping -c 4 8.8.8.8

Got 0% packet loss and stable response times (avg ~78 ms)

Indicates reliable external connectivity

🧾 7. Viewed Network-Related Logs
journalctl | grep -i network
Saw multiple logs related to systemd-resolved, network-online.target, and others

📸 Screenshots Included: all in the image folder
#	Description
1	Created script directory
2	Wrote time-logging script
3	Made script executable & opened crontab
4	Scheduled the job
5	Verified cron is running
6	Viewed IP and routing config
7	Checked network connectivity via ping
8	Viewed logs via journalctl

🧠 Key Skills Practiced:
- Shell scripting and automation
- Cron job setup and verification
- Network diagnostics (IP, ping, routing, logs)
- Log file handling and verification

Next Steps:
- Add log rotation to manage the growing time_log.txt file
- Extend network checks into an uptime monitoring script

