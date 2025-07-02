# ✅ Day 25: Functions, `exit`, Return Codes (`$?`), and `trap`

Today I **continued from the previous day's task** to deepen my understanding of loops and then moved on to complete day 25's task that focuses on scripting best practices like using functions, exit codes, and graceful exits with `trap`.

---

## 🧠 Concepts Practiced

### 1. **Functions in Bash**
Functions let you group reusable commands. Example:

```bash
greet_user() {
  echo "Hello, $1!"
}
greet_user Grace
```

### 2. **Exit Status (`exit` and `$?`)**
Every command returns an exit status:
- `0` = success
- non-zero = failure

You can:
- Use `exit 1` to stop a script early on failure
- Use `$?` to check the result of the last command

Example:
```bash
ls file.txt
"echo $?"
```

### 3. **`trap` Command**
Allows your script to handle interruptions like `Ctrl + C` gracefully.

Example:
```bash
trap "echo 'Script interrupted!'; exit 1" SIGINT
```

---

## 🛠️ Mini Projects

### 🔸 1. **Wait for File Script**
A `while` loop that checks for a file and waits until it appears.

```bash
#!/bin/bash
echo "Enter the full path to the file you're waiting for:"
read filepath

echo "checking for $filepath..."
while [ ! -f "$filepath" ]
do
   echo "File not found."
   sleep 5
done

echo "File found: $filepath"
```


---

### 🔸 3. **Backup Cleanup Script with Function, Exit, and Trap**
```bash
#!/bin/bash

# Function to delete .tmp files
cleanup() {
  echo "Cleaning up .tmp files in $1..."
  find "$1" -type f -name "*.tmp" -delete
  echo "Done cleaning."
}

# Handle Ctrl + C
trap "echo '⛔ Script interrupted. Exiting...'; exit 1" SIGINT

echo "Enter backup directory path:"
read backup_dir

if [ ! -d "$backup_dir" ]; then
  echo "❌ Directory not found."
  exit 1
fi

cleanup "$backup_dir"
echo "✅ Script completed. Exit code: $?"
```

---

## 🖼️ Screenshots Taken

1. Created a `while` loop script to check when a file appears  
2. Ran the script and waited for the file to be created  
3. Opened a second terminal and created the file being monitored  
4. Observed the script detect the file once it appeared  
5. Practiced using `exit` codes to better understand how they work  
6. Wrote a script to demonstrate the use of `exit` and `$?`  
7. Executed the script and checked its exit code  
8. Modified the script to return a custom exit status  
9. Verified the new exit code using `echo $?`  
10. Created a function-based greeting script for practice  
11. Ran the function script and got the expected output  
12. Developed a backup cleaner script using a function and `trap`  
13. Simulated interruption with Ctrl + C to test the `trap` behavior  
14. Confirmed the script completed successfully  
15. Verified `.tmp` files were deleted before and after the cleanup

---

## 🧠 Reflections

- I now understand how scripts can stop themselves with `exit`
- `$?` is very useful for checking the outcome of the last action
- `trap` is great for preventing abrupt exits and giving clear error messages
- Functions make my scripts more organized and reusable

---
