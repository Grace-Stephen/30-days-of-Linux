# ✅ Day 28 of My Linux Learning Journey: Disk Usage Monitoring with Email Alert

Today’s task focused on writing a script to monitor disk usage and send out an **email alert** if usage crosses a set threshold. This involved:

- Writing a monitoring script using `df`, `awk`, and conditionals
- Setting up real email delivery with `msmtp`
- Automating alerts via `cron`

---

## 📜 What I Did

### ✅ Steps Taken

1. **Installed `msmtp` and configured it**  
   - I installed `msmtp`, a lightweight SMTP client, to send emails from the terminal.
   - I then edited its config file to include my Gmail address, SMTP server, and app password.
   - set the file's permission to allow access for only me (`chmod 600 ~/.msmtprc`).

2. **Verified Email Delivery**  
- Verified config worked by sending a test email.
   - Sent an email using:  
     ```bash
     echo "This is a test" | msmtp recipient@example.com
     ```  
   - Received the email in my inbox, confirming setup was successful.

3. **Wrote Disk Usage Monitor Script**  
   - Created a script that checks disk usage and emails me if usage exceeds a certain threshold.

4. **Ran and Tested the Script**  
   - Executed the script to verify that alerts are sent when usage passes the threshold.

5. **Scheduled Script to Run Every Minute via Cron**  
   - Added the script to `crontab -e` with the schedule:
     ```
     * * * * * /home/grace_stephen/disk_alert.sh
     ```
   - Received multiple email alerts as expected.


---

## 📸 Screenshots

1. Installed msmtp and hooked it into the email configuration
2. Created msmtp config file  
3. Edited the config file to contain the app password rather than my usual login password  
4. Sent an email from terminal to confirm it worked  
5. Email received  
6. Created a disk usage monitoring and email alert script  
7. Executed and ran the script  
8. Checked my inbox and saw the email  
9. Used cron to schedule the script to run every minute  
10. Checked my inbox after some minutes and I’ve received lots of emails  

---

## 💡 What I Learned

- How to extract disk usage using `df`, `awk`, `sed`
- How to trigger alerts in scripts using conditionals
- Real-world use of `msmtp` to send email from bash
- Automating monitoring tasks with `cron`

---

✅ **Mini Project Completed:**  
Set up a **disk space monitor** with real email alerts and automated scheduling. A practical tool for system admins!

```bash
chmod +x disk_alert.sh
```

You can stop the cron job anytime with:
```bash
crontab -e
# then delete or comment out the line
```

---
