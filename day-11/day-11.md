# 📁 Day 11: Process Monitoring & Management in Linux

Today’s focus was on understanding and managing processes in Linux using tools like `top`, `ps`, `kill`, and `pkill`. I also simulated background processes using `sleep` and `yes` commands.


---

## 🔧 Summary of Skills Practiced

- Simulated multiple background processes using `sleep` and `yes`
- Monitored processes live with `top` and sorted by memory and CPU usage
- Viewed running processes with `ps aux` and filtered using `grep`
- Terminated specific processes using `kill`
- Used `pkill -f` to kill all processes matching a command

> ✅ *This session strengthened my understanding of how to manage processes on a Linux system. I now know how to monitor system resource usage and safely end unnecessary background processes.*

---

## 📸 Screenshots of Practice

1. ✅ Terminal one – simulated multiple background processes using `sleep`  
2. ✅ Terminal two – simulated multiple background processes using `yes`  
3. ✅ Terminal three – monitored running processes in real time using `top`  
4. ✅ Sorted processes by memory usage using `Shift + M` in `top`  
5. ✅ Sorted processes by CPU usage using `Shift + P` in `top`  
6. ✅ Used `ps aux` to view running processes and filtered for `yes`  
7. ✅ Killed `yes` process using `kill` and confirmed it was terminated  
8. ✅ Used `pkill -f sleep` to kill all sleep processes  

---

## 💡 Key Commands & Concepts

- Run a command in the background:  
  ```bash
  sleep 5000 &
  yes > /dev/null &

Monitor processes in real time with top:
- Press Shift + M → Sort by memory usage
- Press Shift + P → Sort by CPU usage

View running processes:
- ps aux

Filter for a specific process:
- ps aux | grep sleep

Kill a process by PID:
- kill <PID>

Kill all processes matching a command:
- pkill -f sleep