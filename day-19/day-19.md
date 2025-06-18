# 🐧 Day 19 of My Linux Journey – Exploring System Logs & SSH Debugging

## 📚 Focus
- Understanding and monitoring system logs
- Debugging services using log files
- Exploring authentication logs
- Simulating and resolving SSH configuration errors
- Live log monitoring with multiple terminals

---

## ✅ What I Practiced

### 1️⃣ Journalctl Basics
- Viewed all logs:  
  journalctl

- Viewed logs since last boot:
  journalctl -b

- Viewed recent errors in detail:
  journalctl -xe

Checked logs for a specific service (SSH):
  journalctl -u ssh

2️⃣ Log Files in /var/log/
Explored important log files with less and tail -f:

/var/log/syslog

/var/log/auth.log

/var/log/dpkg.log (Debian package logs)

3️⃣ Live Log Monitoring
Used tail -f to monitor logs in real-time while performing actions:
sudo tail -f /var/log/auth.log

- Restarted the Apache2 service from one terminal and watched the output live in another:
sudo systemctl restart apache2

4️⃣ SSH Connection + Live Trigger
SSH-ed into WSL instance from a second terminal to:

Trigger live logs

Observe authentication entries in /var/log/auth.log

5️⃣ Simulating & Fixing SSH Config Errors
Introduced a deliberate error in /etc/ssh/sshd_config

Restart failed:
sudo systemctl restart ssh

- Checked logs to find the cause:
journalctl -u ssh
Fixed the configuration and successfully restarted SSH:

💡 Lessons Learned
journalctl is powerful for tracking down both generic and service-specific issues.

tail -f helps in observing real-time events, useful for monitoring SSH login or service restarts.

/etc/ssh/sshd_config must be syntactically correct — sshd -t is a useful command to test before restarting.

SSH logs appear in /var/log/auth.log, which is crucial for investigating login attempts and failures.

📸 Screenshots
15 screenshots documenting each key task (viewing logs, triggering SSH, monitoring live activity, simulating config errors, and fixing them): all in the image folder
1. Viewed all logs with `journalctl`
2. Viewed logs since the last boot with `journalctl -b`
3. Viewed recent errors in detail with `journalctl -xe`
4. Viewed specific logs for SSH service using `journalctl -u ssh`
5. Explored log files in `/var/log/`
6. Explored `syslog`
7. Explored `auth.log`
8. Explored Debian package manager log (`dpkg.log`)
9. Live monitoring of Apache2 restart in another terminal
10. Output of live log showing Apache2 started
11. Connected via SSH to trigger live log entries
12. Simulated an error in the SSH config file
13. Observed that SSH didn’t restart due to the error
14. Checked logs for the SSH error using `journalctl -u ssh`
15. Fixed the error and confirmed SSH is active again


📁 Files Modified
/etc/ssh/sshd_config

🧠 Commands to Remember
journalctl -xe                 # View recent logs in detail
journalctl -u ssh             # View SSH-specific logs
sudo tail -f /var/log/auth.log  # Live monitor authentication logs
sudo systemctl restart ssh    # Restart SSH service
sudo sshd -t                  # Test SSH config syntax

🔁 Practiced real troubleshooting and monitoring
🧩 Strengthened skills in SSH, journalctl, and log analysis