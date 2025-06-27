# ✅ Day 24: Bash Scripting – Loops (`for` and `while`)

Today’s focus was on understanding and practicing `for` and `while` loops in Bash. I learned how loops work and applied them in a real-world task by analyzing `.log` files inside a directory.

---

## 📚 What I Learned

### 🔁 `for` Loops
- Loops through a list (like files in a directory)
- Used to automate repetitive tasks on each file
- Useful when you already know what you're looping through

### 🔁 `while` Loops
- Repeats a command as long as a condition is true
- Useful when the number of repetitions isn’t fixed. As long as a condition is true, it will run.
- Great for counters, monitoring tasks, or retrying

---

## 🛠️ Mini Project: Log Analyzer Script

I created a simple Bash script to:
- Scan a folder (`admin-project/logs`)
- Loop through all `.log` files
- Print total number of lines and how many contain the word “error”

### ✅ For Script Used
```bash
#!/bin/bash

echo "Enter the path to the folder containing .log files:"
read log_dir

if [ ! -d "$log_dir" ]; then
    echo "Directory does not exist."
    exit 1
fi

for logfile in "$log_dir"/*.log
do
    if [ -f "$logfile" ]; then
        echo "Analyzing $logfile"
        total_lines=$(wc -l < "$logfile")
        error_lines=$(grep -i "error" "$logfile" | wc -l)
        echo "Total lines: $total_lines"
        echo "Lines with 'error': $error_lines"
        echo "-----------------------------"
    fi
done
```

---

## 🔂 While Loop Practice

I also created a simple script to practice how `while` works.

### ✅ While Script
```bash
#!/bin/bash

count=1
while [ $count -le 5 ]
do
    echo "This is loop iteration $count"
    ((count++))
done
```


## 📸 Screenshots: all in the image folder

1. log analyzer script  
2. the directory I will test the script with  
3. ran the script and entered the directory  
4. got an error - no such file or directory  
5. modified the script  
6. running the modified script returned the expected output  
7. viewed the content of the file that the script looped through
8. added lines containing error to the file for testing  
9. it returned 4 lines with error this time — it was 1 line earlier  
10. ran the script in my home directory  
11. created a script to practice `while`  
12. output of running the `while` script  
---

## ✅ Summary

Today’s task helped me:
- Understand and apply loops in Bash
- Work with `.log` files in a real project folder
- Troubleshoot and test with custom input
- Learn the difference between `for` and `while`

