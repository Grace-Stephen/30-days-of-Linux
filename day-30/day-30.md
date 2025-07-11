# ✅ Day 30 of Linux — User Creation Via Script, Group Assignment & Home Directory Backup Automation

On the final day of this Linux journey, I automated a common sysadmin task — **bulk user creation** with added functionality to set passwords, assign groups, and archive each user’s home directory. This simulated a real-world scenario where system administrators onboard multiple users at once.

---

## 💡 What I Learned

- How to read user data from a file
- How to create users via script
- How to assign users to a group
- How to archive user home directories for backup
- How to debug and fix errors (like file path issues)

---

## 🛠️ Key Concepts Practiced

- `useradd`, `usermod`, `passwd` commands
- File handling and loops in bash
- `tar` for archiving home directories
- Error handling and directory checks

---

## 📂 Project Structure

```bash
linux-day30/
├── user_list.txt             # Contains the list of users to be created
├── user_create.sh            # Main script that automates user creation and backup
└── backups/                  # Output directory where user home directories are archived

📸 Screenshots and Tasks
Step	Description
1️⃣ Created a file containing a list of users
2️⃣ Created the user creation script
3️⃣ Continuation of the user creation script
4️⃣ Executed and ran the script but got an error due to file path
5️⃣ Switched directory and ran the script – it ran successfully
6️⃣ Confirmed user and group creation
7️⃣ Checked home directories and backups
8️⃣ Viewed the content of two archives

## Sample Code: user_create.sh
#!/bin/bash

# Ask user for the filename containing user:group info
echo "Enter the name of the user file (e.g., users.txt):"
read userfile

# Check if the file exists
if [ ! -f "$userfile" ]; then
  echo "File $userfile not found!"
  exit 1
fi

# Read each line of the file (username:groupname format)
while IFS=: read -r username groupname; do
  # Skip empty lines or lines starting with #
  [[ -z "$username" || "$username" =~ ^# ]] && continue

  # Create the group if it doesn't already exist
  if ! getent group "$groupname" > /dev/null; then
    echo "Creating group: $groupname"
    groupadd "$groupname"
  fi

  # Create the user with home directory
  echo "Creating user: $username"
  useradd -m "$username"

  # Set default password for user
  echo "$username:Password123" | chpasswd

  # Add user to the group
  usermod -aG "$groupname" "$username"
  echo "User $username added to group $groupname."

  # Archive the user's home directory
  home_dir="/home/$username"
  if [ -d "$home_dir" ]; then
    tar -czf "/home/${username}_home_backup.tar.gz" "$home_dir"
    echo "Archived $username's home directory to /home/${username}_home_backup.tar.gz"
  else
    echo "Home directory for $username not found, skipping archive."
  fi

done < "$userfile"

✅ Output
Created users listed in user_list.txt

Verified their home directories

Archived home directories to backups/

Saw the archive contents with tar -tf

🧠 Reflection
This task helped reinforce:
- File parsing
- System automation
- Command chaining and scripting best practices

I'm proud to have completed this 30-day challenge! 🎉
