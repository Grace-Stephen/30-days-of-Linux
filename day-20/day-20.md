# 🗓️ Day 20 - Scheduled Tasks in Linux

Today I practiced **automating recurring and one-time tasks** using `cron` and `at` — two powerful tools every Linux system administrator must know.

---

## ✅ Tasks Practiced: screenshots of practice are in the images folder

### 1. Opened the crontab file using nano
- 📸 *Screenshot 1*
- Ran `crontab -e` and selected nano as the default editor.

### 2. Added a scheduled task
- 📸 *Screenshot 2*
- Wrote a cron job to run a script at a specified time.

### 3. Viewed scheduled tasks
- 📸 *Screenshot 3*
- Used `crontab -l` to confirm that the job was saved successfully.

### 4. Installed and practiced using `at`
- 📸 *Screenshot 4*
- Installed the `at` utility and scheduled a one-time task with:
  ```bash
  echo "echo 'System check at $(date)' >> ~/check.log" | at now + 1 minute

5. Verified the one-time job was scheduled
📸 Screenshot 5
- Used atq to check the queue of scheduled at jobs.

6. Created directories for the automation project
📸 Screenshot 6

- Set up folder structure:
~/admin-project/
  ├── logs/
  ├── backup/
  └── scripts/

7. Wrote an automation script to back up logs
📸 Screenshot 7

Script: backup_logs.sh

Backs up /var/log/syslog to the backup folder with a date-stamped filename.

Appends a success message with a timestamp to job.log.

📝 Brief explanation:
I wrote an automation script that creates a file to back up logs from /var/log/syslog, and another file (job.log) to log evidence that the script successfully ran.

8. Made the script executable
📸 Screenshot 8
- Used chmod +x backup_logs.sh

9. Scheduled the backup script to run daily at 1 AM
📸 Screenshot 9
- Cron job added:
0 1 * * * /home/grace/admin-project/scripts/backup_logs.sh

10. Created a weekly cleanup script
📸 Screenshot 10
- Script: cleanup_backups.sh

- Deletes backup files older than 7 days.

- Appends a message to job.log.

11. Scheduled the cleanup to run every Sunday by 2AM
📸 Screenshot 11
- Cron job added:
0 2 * * 0 /home/grace/admin-project/scripts/cleanup_backups.sh

12. Simulated a one-time job again to confirm understanding
📸 Screenshot 12
- Confirmed that at executed the job and appended a text to job.log.

🧠 Key Concepts Learned
- The difference between cron (repeating tasks) and at (one-time tasks).
- Proper cron time format: minute hour day month weekday.

Best practices:
- Use absolute paths in cron jobs.
- Always log script execution to verify automation.
- Use chmod +x to make scripts executable.
- File structure and naming conventions for maintainable backups.