# 📁 Week 1: Linux Practice – File Management & Permissions

This week focused on mastering file and directory manipulation particularly creating/navigating nested folder structure. It was also a deep dive into recursive operations, search tools (`grep` & `find`), ownership, and permission settings in Linux. Each task helped reinforce real-world command-line administration skills.

---

## 🔧 Summary of Skills Practiced

- **`mkdir -p`** – Create nested directories in one command.
- **`touch`** – Create new empty files.
- **`echo >`** – Write content into files from the CLI.
- **`mv`, `cp`, `rm`** – Move, copy, and delete files and directories.
- **`grep`, `find`** – Search for files and content inside files.
- **`chmod`, `chown`, `su`** – Modify permissions and ownership.
- **`ls -l`, `cat`, `head`, `tail`, `less`** – View file info and content.

> ✅ *This week helped me understand how Linux handles file structures, permissions, and basic system operations.  
> I also practiced switching users, restricting folder access, and working with groups.*

---

## 📸 Screenshots of Practice

### 1️⃣ Created nested folder structure using `mkdir -p`
![1-created nested structure](images/1.png)

### 2️⃣ Created empty files in specific folders using `touch`
![2-created files](images/2.png)

### 3️⃣ Wrote content into a file with `echo >`
![3-added content to a file](images/3.png)

### 4️⃣ Viewed file contents using `cat`
![4-viewed file content](images/4.png)

### 5️⃣ Moved script file from one directory to another
![5-moved file](images/5.png)

### 6️⃣ Copied a file within nested directories
![6-copied file](images/6.png)

### 7️⃣ Used `grep` to search for keywords & `find` for filenames
![7-used grep and find](images/7.png)

### 8️⃣ Changed group ownership of a folder using `chown`
![8-changed group ownership](images/8.png)

### 9️⃣ Updated folder permissions with `chmod`
![9-changed folder permission](images/9.png)

### 🔟 Switched user account using `su` to test access
![10-switched user](images/10.png)

### 1️⃣1️⃣ Moved entire folder to a different directory
![11-moved folder](images/11.png)

### 1️⃣2️⃣ Tested permission setups by modifying access
![12-tested permissions](images/12.png)

### 1️⃣3️⃣ changed group ownership of folders in a nested folder structure
![13-changed group ownership](images/13.png)

### 1️⃣4️⃣ Restricted group access for subfolders in a directory
![14-restricted group access](images/14.png)

---

### SOME KEY TAKEAWAYS
KEY TAKEAWAYS FROM WEEK 1 PROJECT
- you can create multiple folders with one line of command
- use touch to create empty files in each of the folders
- use echo to add content while creating a file
- move files from subfolders to main folder
- use grep to search for a keyword in a folder and its subfolders by including -r
- use cat >> to append texts to a file or cat > to overwrite content in a text
- you have to enter the right folder hierachy in your command when working with nested folders. 
- in a nested folder, when assigning permissions, you have to ensure the group or user has execute permission on all paths leading to the folder you want them to access or it won’t work. 
- For files: You don't need execute permission to read/write.
- For directories: You must have execute permission for that directory in order to access or write to anything inside the directory, even if you have r or w permission.