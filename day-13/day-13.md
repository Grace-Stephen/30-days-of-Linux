# Day 13 – System Info and Disk Usage

Today I practiced how to check various system and disk usage information using Linux commands. These are useful for monitoring, troubleshooting, and understanding system health.

## ✅ What I Practiced:

1. **Checked server’s name and architecture**  
   → Used `uname -a` and `hostname` to display the system’s kernel, architecture, and hostname.

2. **Checked how long the server has been up**  
   → Used `uptime` to see how long the system has been running, number of users, and load averages.

3. **Checked overall disk usage**  
   → Used `df -h` to show available and used disk space on all mounted filesystems in a human-readable format.

4. **Checked free memory and swap space**  
   → Used `free -h` to display total, used, and free memory (RAM) and swap space.

5. **Checked which folder or file is using the most disk space**  
   → Used `du -sh *' to check disk usage in my current directory.

6. **Checked disk usage of another directory**  
   → Repeated `du -sh /opt' to check disk usage in opt directory.

## 🖼️ Screenshots:

- `1` – Checked server's name and architecture  
- `2` – Checked how long the server has been up  
- `3` – Used `df -h` to check overall disk usage  
- `4` – Used `free -h` to check memory and swap space  
- `5` – Used `du -sh` to identify largest space usage in a directory  
- `6` – Checked another directory's disk usage  

## 🧠 What I Learned:

- `df -h` gives a snapshot of all mounted storage devices and their usage.
- `free -h` is helpful to monitor memory usage including swap.
- `du -sh` is useful for drilling into which directories are using the most disk space.
- I discovered that WSL (Windows Subsystem for Linux) shows virtual mounts and can assign seemingly large disk space (e.g., 1TB) even if the actual Windows disk is smaller.