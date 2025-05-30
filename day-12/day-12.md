Day 12: Background Processes & Job Control in Linux
Today’s focus was on managing background processes, job control, and disowning or logging command output using &, jobs, fg, bg, nohup, and ps. I explored how to run processes in the background, monitor their status, and bring them back to the foreground when needed.

Summary of Skills Practiced
- Launched commands to run in the background with &
- Monitored jobs using jobs and ps aux | grep
- Paused and resumed jobs with Ctrl + Z, bg, and fg
- Logged command output using nohup and redirected it to a file
- Interpreted job IDs and process IDs

Investigated real-world use of background processes like ping and top

✅ This session helped me gain confidence in multitasking within the terminal, which is crucial when managing multiple processes like service monitoring, long-running commands, or scripts in server environments.

📸 Screenshots of Practice
image 1: Tested what happens when I bring a sleep process to the foreground
image 2: Used ps aux | grep to locate the ping process and terminated it
image 3: Practiced pausing a foreground process (sleep) and restarting it in the background
image 4: Started a nohup ping to google.com and a top process with logging
image 5: Verified background jobs using the jobs command
image 6: Observed that the top process finished after 5 iterations and no longer appeared in jobs
image 7: Checked the output log of the top process for system stats
image 8: Brought a background job to the foreground using fg %job_number

💡 Key Commands & Concepts
Run a command in the background:
- sleep 1000 &

View jobs started in the current shell:
- jobs

Bring a job to the foreground:
- fg %1

Pause a running foreground process:
- (Press) Ctrl + Z

Resume a stopped job in the background:
- bg %1

Start a long-running process with logging (ignores hangup):
- nohup ping google.com > google_ping.txt &

Monitor system usage in batch mode and log:
- nohup top -b -n 5 > top_output.txt &

Check specific running processes (e.g., ping):
- ps aux | grep ping

Real-World Use Cases
- Server Health Monitoring: Use nohup ping to continuously check server reachability and log downtimes.

- Performance Logging: Use top or htop in batch mode to capture CPU/memory usage snapshots at intervals.

- Script Execution: Run backups, updates, or data migration scripts in the background to avoid blocking your terminal.

- Troubleshooting: Restart or monitor services without stopping other critical terminal tasks.