# 📁 Day 6: Linux Practice – File Searching & Content Searching

Today’s focus was on using the `find`, `locate`, and `grep` commands to search for files, folders, and file content effectively. This helped strengthen understanding of how Linux handles file structures and command-line tools for discovery and inspection.

---

## 🔍 Summary of Tools Used

- **`find`** – Used to search for files/folders with specific attributes (name, modification time, size, permissions, etc.).
- **`locate`** – Used for fast file searching based on name only. Faster but may require updating the file database with `updatedb`.
- **`grep`** – Used to search **inside** files for specific content.

> ✅ *So we use `find` and `locate` when searching for files and folders. `grep` is used when searching for content in a file. `locate` is better for quick name-based searches. `find` is more flexible — allowing filtering by date, size, permission, and even running actions like delete.  
>
> Used `grep -i` to enable case-insensitive search.  
> Used `grep -r` to search for a word in all the files and folders in a directory.*
>
> *Before I started practicing, I first installed `locate` in my WSL Ubuntu so I could use the `locate` command.*

---

## 📸 Screenshots of Practice

### 1️⃣ Searched for a file using `find`
![1-searched for a file using find](images/1-searched.png)

### 2️⃣ Tried searching for a file I created using `find`
![2-tried searching](images/2-tried.png)

### 3️⃣ Used `find` to locate files modified in the last 3 days in /var/log
![3-used find to find files modified](images/3-modified-3-days.png)

### 4️⃣ Also searched for modified files in my home directory
![4-also used find](images/4-home-dir-search.png)

### 5️⃣ Practiced using `locate`
![5-practiced using locate](images/5-locate.png)

### 6️⃣ Used `find` to look for files with specific permissions
![6-used find to look for permissions](images/6-permissions.png)

### 7️⃣ Used `find` for files of specific size & `locate` to find files by name
![7-used find for size](images/7-find-size-locate.png)

### 8️⃣ Used `grep` to find a keyword in a file
![8-find a keyword](images/8-grep-keyword.png)

### 9️⃣ Used `grep -i` for case-insensitive content search
![9-used grep -i](images/9-grep-i.png)

### 🔟 Used `grep -r` to search across all folders in a directory
![10-grep -r](images/10-grep-r.png)

---

## 🧠 Commands Practiced

# Find all .log files in /var/log
find /var/log -type f -name "*.log"

# Find files modified in the last 3 days
find /var/log -type f -mtime -3


# Update locate database
sudo updatedb

# Locate a file by name
locate passwd

# Grep content in a file
grep "sudo" /etc/passwd

# Grep case-insensitive
grep -i "Ubuntu" filename.txt

# Grep recursive through a directory
grep -r "sudo" /etc/
