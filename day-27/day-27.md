# 🗂️ Day 27: Backup Script with Timestamp

## ✅ Today's Task
- Create a script that compresses a directory
- Automatically adds a timestamp to the archive name
- Stores the archive in a `backup` folder

---

## 🧠 What I Practiced
- `tar -czf` for archiving and compression
- Dynamic filenames with `$(date)` timestamps
- Using variables for paths and filenames
- Creating directories using `mkdir -p`
- Adding validation to check if the directory exists before proceeding

---

## 🛠️ Script: `backup_with_timestamp.sh`

```bash
#!/bin/bash

read -p "Enter the full path of the directory you want to back up: " source_dir

if [ ! -d "$source_dir" ]; then
  echo "❌ Directory not found. Exiting."
  exit 1
fi

backup_dir="$HOME/backup"
mkdir -p "$backup_dir"

timestamp=$(date +"%Y-%m-%d_%H-%M-%S")
archive_name="${source_dir##*/}_$timestamp.tar.gz"

tar -czf "$backup_dir/$archive_name" "$source_dir"

echo "✅ Backup complete! File saved as: $backup_dir/$archive_name"
```

---

## ▶️ How I Ran It
```bash
chmod +x backup_with_timestamp.sh
./backup_with_timestamp.sh
```

---

## 📸 Screenshots & What They Show

| Screenshot | Description |
|-----------|-------------|
| ![1](../images/day27/1.png) | 1. Created a backup script with timestamp |
| ![2](../images/day27/2.png) | 2. Ran the script |
| ![3](../images/day27/3.png) | 3. Viewed the archived file and its content |

---

## ✅ Sample Output
```
Enter the full path of the directory you want to back up: /home/grace_stephen/admin-project
✅ Backup complete! File saved as: /home/grace_stephen/backup/admin-project_2025-07-02_14-46-26.tar.gz
```

Used this command to inspect:
```bash
tar -tf ~/backup/admin-project_2025-07-02_14-46-26.tar.gz
```

---

## 📘 What I Learned
- How to safely check if a directory exists using `if [ ! -d "$source_dir" ]`
- How to append timestamps to filenames dynamically
- Importance of using `~/` or full paths when referencing files
- How `tar` handles compression and archiving in one command

---

