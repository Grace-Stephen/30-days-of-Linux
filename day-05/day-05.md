# Day 5: Linux File Permissions & Ownership

## 📌 Objective

To understand and practice Linux file permissions, ownership, and user/group management commands including `ls -l`, `chmod`, `chown`, and `chgrp`.

---

## 🛠️ Commands Practiced

- `adduser` – create a new user
- `groupadd` – create a new group
- `usermod -aG` – add a user to a group
- `ls -l` – list file permissions
- `chmod` – change file permissions
- `chown` – change file owner
- `chgrp` – change group ownership

---

## 🧪 Steps Taken

### 1. ✅ Created Users for File Permission Practice

Created new users using `sudo adduser` to simulate different access levels.

![Created users for file permission practice](images/1%20created%20users%20for%20file%20permission%20practice.png)

---

### 2. 🔍 Viewed and Changed File Permissions

Used `ls -l` to inspect permissions and `chmod` to modify them.

![Viewed file permissions and changed permissions](images/2%20viewed%20file%20permissions%20and%20changed%20perm.png)

---

### 3. 👥 Created a New Group and Added Users

Used `groupadd` and `usermod -aG` to create a new group and add users.

![Created a new group and added users](images/3%20created%20a%20new%20group%20and%20added%20two%20users.png)

---

### 4. 🔄 Changed File Ownership

Used `sudo chown` to update file and group ownership.

![Changed user and group ownership](images/4%20changed%20user%20and%20group%20ownership%20of%20a%20file.png)

---

### 5. 🔐 Modified Group Permissions

Used `chmod` to assign read and execute permissions to the group.

![Changed the group permission](images/5%20changed%20the%20group%20permission%20from%20zero%20t.png)

---

## 📚 What I Learned

- How file permissions work in Linux (read=4, write=2, execute=1).
- The difference between user, group, and others permissions.
- How to create and manage users and groups.
- How to test permission changes effectively.
- The role of `sudo` and how it can bypass normal restrictions.

---

## 🚀 Next Steps

- Practice more commands for file navigation and file management

---

📁 _All screenshots are stored in the `/images` folder for easy reference._
