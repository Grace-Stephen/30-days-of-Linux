# 👤 Day 8: Linux User Management

This day focused on the fundamentals of Linux user management. I practiced creating users, assigning passwords, changing usernames and home directories, locking/unlocking user accounts and safely deleting user accounts. These are essential operations for system administrators responsible for managing access to Linux systems.

---

## 🔧 Summary of Skills Practiced

- **`whoami`, `id`** – Checked current user and identity details.
- **`adduser`** – Created a new user with default home directory.
- **`passwd`** – Set or changed user passwords.
- **`grep /etc/passwd`** – Verified user creation in the system.
- **`usermod -l`** – Renamed a user.
- **`usermod -d -m`** – Renamed user home directory and moved files.
- **`deluser --remove-home`** – Deleted user and cleaned up home directory.
- **`usermod -L / -U`** – Locked and unlocked user accounts.

> ✅ *Practicing these commands gave me real confidence in managing local users, a task common in production servers and WSL/Ubuntu systems.*

---

## 📸 Screenshots of Practice

### 1️⃣ Checked current user, created a new user using `adduser`
![1-whoami-id](images/1-whoami-id.png)

### 2️⃣ Changed user password and confirmed creation with `grep`
![2-passwd-grep](images/2-passwd-grep.png)

### 3️⃣ Viewed WSL home directories before user renaming
![3-gui-before-change](images/3-gui-before-change.png)

### 4️⃣ Renamed user and home folder, then verified from GUI
![4-gui-after-change](images/4-gui-after-change.png)

### 5️⃣ Used CLI to verify renamed user and updated home path
![5-cli-rename](images/5-cli-rename.png)

### 6️⃣ Deleted user and home directory using `deluser --remove-home`
![6-delete-user](images/6-delete-user.png)

### 7️⃣ Locked and unlocked the user account, tested login restrictions
![7-lock-unlock](images/7-lock-unlock.png)

---

## 💡 Key Takeaways

- Every new user created with `adduser` automatically gets a home directory at `/home/username`.
- Use `grep username /etc/passwd` to check if a user exists in the system.
- Renaming a user with `usermod -l` does **not** rename their home directory by default — use `-d /home/newname -m` to move it.
- Deleting a user with `deluser` doesn’t remove their home unless you add `--remove-home`.
- Locking a user disables their login but keeps the account intact (`usermod -L` and `-U`).
- Always validate changes from both the terminal and GUI (especially in WSL or desktop environments).

---

✅ Day 8 helped build a solid foundation in Linux identity and access management. These skills are directly transferable to real-world Linux server management.
