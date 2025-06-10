# 🐧 Linux Command Line Practice – Day 15

## 📅 Week 3 | Day 15: Package Management & System Monitoring Tools

### 🧠 Skills Covered
- Managing packages with `apt` (Ubuntu)
- Exploring interactive monitoring tools (`htop`)
- Logging IT support actions

---

### 📘 Scenario Simulated
You're configuring a newly installed Ubuntu system for a junior staff member who needs basic system monitoring tools. Your task is to update the system, install `htop`, explore and document its usage, and finally uninstall it. You’ll also practice proper documentation by capturing screenshots of each step.

---

### 💼 Tasks & Commands

#### ✅ 1. Update and Upgrade the System
```bash
sudo apt update && sudo apt upgrade -y
```
📸 *Screenshot:* `1 updating and upgrading ubuntu.png`

---

#### ✅ 2. Install htop
```bash
sudo apt install htop 
```
📸 *Screenshot:* `2 installed htop.png`

---

#### ✅ 3. Launch htop and Sort by CPU Usage
```bash
htop
# Press F6 → Choose "CPU%" to sort
```
📸 *Screenshot:* `3 sort process by CPU.png`

---

#### ✅ 4. Explore Columns in htop with F6
Use `F6` to customize the columns displayed in `htop`.

📸 *Screenshot:* `4 exploring htop with f6.png`

---

#### ✅ 5. Sort by Memory Usage
```bash
# In htop, press F6 → Choose "MEM%" to sort
```
📸 *Screenshot:* `5 sort by memory.png`

---

#### ✅ 6. Kill a Process with SIGKILL
```bash
# In htop, navigate to a process → Press F9 → Choose signal 9 (SIGKILL)
```
📸 *Screenshot:* `6 used sigkill signal to kill a process.png`

---

#### ✅ 7. View Process Tree
```bash
# In htop, press F5 to toggle Tree view
```
📸 *Screenshot:* `7 tree view of a process.png`

---

#### ✅ 8. Uninstall htop
```bash
sudo apt remove htop 
```
📸 *Screenshot:* `8 uninstalled.png`

---

### 📄 Documentation Tip
Log your observations from htop into a Notion, Google Doc, or markdown file. Include details like:
- CPU usage
- Memory allocation
- Number of tasks and load averages
- Any processes you found interesting or resource-heavy

---

### 📁 Screenshot Summary

| Step | Action | Screenshot |
|------|--------|------------|
| 1 | Update system | `1 updating and upgrading ubuntu.png` |
| 2 | Install htop | `2 installed htop.png` |
| 3 | Sort by CPU | `3 sort process by CPU.png` |
| 4 | Explore F6 | `4 exploring htop with f6.png` |
| 5 | Sort by memory | `5 sort by memory.png` |
| 6 | Kill a process | `6 used sigkill signal to kill a process.png` |
| 7 | Tree view | `7 tree view of a process.png` |
| 8 | Uninstall htop | `8 uninstalled.png` |

---

### 🧩 Reflection
Today’s task simulated a real IT support/package management activity: setting up monitoring tools, using them, and cleanly uninstalling them. 
