# 🗂️ Day 29 - Linux Practice: Combine Multiple Scripts into a Toolkit

Today’s task was about **consolidating multiple useful Bash scripts into a single interactive toolkit**. This means creating a master script that gives users a menu to choose which script to run, enhancing productivity and organization.

---

## ✅ What I Practiced

- Created a `toolkit` directory to organize scripts
- Wrote a launcher script using a menu system (`case` statement)
- Integrated multiple existing scripts:
  - File checker
  - Log analyzer
  - Wait for file detector
  - Disk usage alert script
- Practiced organizing and reusing code

---

## 🛠️ Toolkit Menu Script

```bash
#!/bin/bash

while true; do
    clear
    echo "============== Linux Toolkit =============="
    echo "1. Check File Details"
    echo "2. Analyze .log Files"
    echo "3. Wait for a file"
    echo "4. Monitor Disk Usage"
    echo "5. Exit"
    echo "==========================================="
    read -p "Choose an option [1-5]: " choice

    case "$choice" in
        1)
            bash check_file.sh
            read -p "Press Enter to return to menu..."
            ;;
        2)
            bash log_analyzer.sh
            read -p "Press Enter to return to menu..."
            ;;
        3)
            bash wait_for_file.sh
            read -p "Press Enter to return to menu..."
            ;;
        4)
            bash disk_alert.sh
            read -p "Press Enter to return to menu..."
            ;;
        5)
            echo "Goodbye!"
            exit 0
            ;;
        *)
            echo "Invalid option. Try again."
            sleep 1
            ;;
    esac
done

📸 Screenshots: all in images folder
1. Created a toolkit directory and copied my working scripts into it

2. Created a launcher menu script

3. Executed and ran the script

4. Selected option 1 - file checker

5. Selected option 2 - log analyzer

6. Selected option 3 - wait for file and created an empty file in another terminal

7. Selected option 4 - disk usage alert

8. Disk alert email received

🧠 What I Learned
- How to build a modular and reusable set of scripts

- How to guide users with interactive menus using case statements

- How to combine existing tools for better efficiency

