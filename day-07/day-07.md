# Day 7 - Linux Practice: File & Directory Permissions (Continued from Day 5)

## 📝 Summary

On Day 7, I built on what I learned in Day 5 about file permissions by testing the permissions I assigned to a group.

### 🔧 Scenario

- I created a file `file.txt` and gave the **DevOps group** permission to read and execute it.
- A user `zion`, who is a member of the **DevOps group**, tried to access `file.txt`.
- The file was inside `ogomafolder`, which was in the home directory.
- Zion couldn’t access the file or even list the contents of the folder.

### 🧠 Lesson Learned

Even if a user has group permission to a file, they **cannot access the file unless they have execute permission on the directory** it's in.

### 🛠️ What I Did

1. Logged out as zion back into my admin account.
2. Confirmed `zion` was part of the `devops` group.
3. Realized directory permission was the issue.
4. Moved `ogomafolder` to `/opt` since I couldn’t safely modify permissions on the `/home` directory.
5. Set appropriate ownership and group permissions on `/opt/ogomafolder`.
6. Verified `zion` could now access `file.txt`.
7. Noticed he also had access to other files in that folder like 'mynotes' so I restricted access to that file.
8. Experimented with `sudo`, `nano`, and navigating directories to confirm file permission behavior.

---

## 📸 Screenshots


1. ![Logged in as zion](your-repo-path/1-logged-in-as-zion.png)
2. ![ls ogomafolder but no access](your-repo-path/2-ls-ogomafolder-but-no-access.png)
3. ![Zion is in devops group](your-repo-path/3-zion-in-devops-group.png)
4. ![Moved filetxt to ogomafolder](your-repo-path/4-logged-out-and-moved.png)
5. ![Still can't view folder](your-repo-path/5-cant-view-folder.png)
6. ![Realized permission issue](your-repo-path/6-realized-permission-issue.png)
7. ![Changed ownership](your-repo-path/7-changed-ownership.png)
8. ![Zion can now view file](your-repo-path/8-logged-in-can-view.png)
9. ![cd for navigation](your-repo-path/9-cd-for-navigation.png)
10. ![View folders in ogomafolder](your-repo-path/10-realized-folder-visible.png)
11. ![Modified directory permissions](your-repo-path/11-modified-permissions.png)
12. ![Can't ls ogomafolder](your-repo-path/12-cant-ls-ogomafolder.png)
13. ![nano to test](your-repo-path/13-nano-test.png)
14. ![Zion can access other files](your-repo-path/14-access-other-files.png)
15. ![No access to mynotes](your-repo-path/15-no-access-to-mynotes.png)
16. ![Tested with sudo](your-repo-path/16-tested-with-sudo.png)

---

## ✅ Key Commands Used

su - username
ls
ls -la
getent group groupname
cat
mv
pwd
chmod
chgrp
cd
nano


