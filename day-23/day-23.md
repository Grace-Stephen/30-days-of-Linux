# 🐧 Day 23: Bash Scripting – Conditions and If Statements

## ✅ Objective
Learn how to use conditional statements in bash:
- `if`, `else`, `elif`
- `[ condition ]` / `test`
- File test operators like `-e`, `-f`, `-s`, `-r`

---

## 📂 Task
Write a bash script that:
- Prompts the user for a file path
- Checks if the file exists
- Tells if it's a regular file or a directory
- States whether it’s empty or not
- Reports read permission status

---

## 🛠️ Script: `check_file.sh`

```bash
#!/bin/bash
echo "Enter the file path you want to check:"
read filepath
if [ -e "$filepath" ]; then
echo "File exists."
if [ -f "$filepath" ]; then
echo "it is a regular file."
if [ -s "$filepath" ]; then
echo "file is not empty."
else
echo "file is empty."
fi
if [ -r "$filepath" ]; then
echo "you have read permission."
else
echo "you do NOT have read permission."
fi
elif [ -d "$filepath" ]; then
echo "this is a directory, not a file."
else
echo "it is not a regular file (maybe a special file)."
fi
else
echo "file does not exist."
fi
```

---

## 🧪 How I Tested

### 🔹 Testing & Debugging Flow : all screenshots are in the images folder

| Screenshot | Description |
|-----------|-------------|
| ![1](./screenshots/1.png) | 1. Created a script that provides info about files |
| ![2](./screenshots/2.png) | 2. Got a syntax error when I ran the script |
| ![3](./screenshots/3.png) | 3. Fixed the error – used `it is` instead of `it's` |
| ![4](./screenshots/4.png) | 4. Got an error again |
| ![5](./screenshots/5.png) | 5. Error spotted – double quote before `echo` and missing `fi` block |
| ![6](./screenshots/6.png) | 6. Ran the script and got the expected output for the directory |
| ![7](./screenshots/7.png) | 7. Ran the script for a file I had no permission to access |
| ![8](./screenshots/8.png) | 8. Ran the script for a file that does not exist |
| ![9](./screenshots/9.png) | 9. Ran the script with a full file path |
| ![10](./screenshots/10.png) | 10. Enhanced the script to say when it is a directory |
| ![11](./screenshots/11.png) | 11. Before vs. after the script was enhanced |
| ![12](./screenshots/12.png) | 12. Made it possible for all users to run the script system-wide |
| ![13](./screenshots/13.png) | 13. Logged in as another user to confirm accessibility |

---

## 🚀 Improvements Made
- Removed contractions to fix syntax error
- Identified and resolved misplaced quotes
- Added check for directory with `elif [ -d ... ]`
- Made the script globally executable and usable

---

## ✅ What I Learned
- How to use `if`, `else`, and `elif` for decision-making in Bash
- How to check file properties using flags like `-e`, `-f`, `-s`, `-r`, `-d`
- How to troubleshoot and debug syntax errors in scripts
- How to make scripts globally accessible to any user
- Importance of quoting variables and prompting users clearly

---

## 💡 Next Step (Day 24 Preview)
Learn about **loops** in Bash and how to iterate through files or commands using `for` and `while`.

