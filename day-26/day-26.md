# ✅ Day 26: User Input and `case` Statement in Bash

Today, I learned how to:
- Accept input from the user using `read`
- Use a `case` statement to handle multiple input options

This is a powerful alternative to using multiple `if` or `elif` blocks, especially when handling menu-style input.

---

## 🧠 Concepts Practiced

### 🔹 Taking User Input
```bash
echo "What is your name?"
read username
echo "Welcome, $username!"
```
- `read` pauses and waits for user input
- The value is stored in a variable and can be used throughout the script

---

### 🔹 `case` Statement
## 🛠️ Mini Project: Task Manager Script

I created a script called `task_menu.sh` that performs different system tasks based on user input.

### 📜 Code:
```bash
#!/bin/bash

echo "Welcome to the system task menu!"
echo "Please select an option:"
echo "1) Check disk usage"
echo "2) Show running processes"
echo "3) Show current date and time"
echo "4) Exit"

read -p "Enter your choice [1-4]: " choice

case $choice in
  1)
    echo "Checking disk usage..."
    df -h
    ;;
  2)
    echo "Showing running processes..."
    ps aux
    ;;
  3)
    echo "Current date and time:"
    date
    ;;
  4)
    echo "Goodbye!"
    exit 0
    ;;
  *)
    echo "Invalid option. Please run the script again."
    ;;
esac
```

### 🧪 How I ran it:
```bash
chmod +x task_menu.sh
./task_menu.sh
```

---

## 🖼️ Screenshots Taken: all in the images folder

1. Wrote a simple script to practice user input
2. executed and ran the script
3. Created a mini task manager script  
4. Ran the script and selected option 1  
5. Ran it again and selected option 2  
6. Ran it again and selected option 3  
7. Entered 4  
8. Entered an invalid option  

---

## 💡 Reflections
- `case` is cleaner than stacking many `if` or `elif` statements
- User input adds interaction to my scripts, making them more dynamic
- I now feel more confident building interactive Bash scripts

---
