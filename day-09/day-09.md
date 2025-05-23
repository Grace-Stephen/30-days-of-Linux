# 📁 Day 9: Linux Practice – Shared Group Folder with SetGID

Today's practice was focused on setting up a shared folder for multiple users using Linux permissions and group management. I learned how to make sure all users in the same group can collaborate smoothly by setting up directory ownership and using the `SetGID` permission.

---

## 🔧 Summary of Skills Practiced

- **`groupadd`** – Create a new user group.
- **`usermod -aG groupname username`** – Create new users and assign them to a group.
- **`chown :groupname`** – Change the group ownership of a directory.
- **`chmod 770`** – Set full permissions for owner and group, none for others.
- **`chmod g+s`** – Set the SetGID bit so new files inherit group ownership.
- **`echo >>`** – Append text into files from the command line.
- **User Switching** – Use different users to test access and file creation.

> ✅ *This exercise helped reinforce how shared directories work and how to manage collaboration through group permissions.*

---

## 📸 Screenshots of Practice

### 1️⃣ Created a `network` group and two users
![1-created network group and users](images/1.png)

### 2️⃣ Added the two users to the `network` group and created the directory
![2-added users to group and created directory](images/2.png)

### 3️⃣ Assigned group ownership and gave the folder access permissions
![3-assigned group and set permissions](images/3.png)

### 4️⃣ Enabled SetGID so all files inherit the group `network`
![4-setgid activated](images/4.png)

### 5️⃣ Signed in as one user and created a file to test group permission
![5-tested with user1](images/5.png)

### 6️⃣ Signed in as another user and confirmed she could access/write
![6-tested with user2](images/6.png)

### 7️⃣ Bonus: Appended text to an existing file using `echo >>`
![7-echo append](images/7.png)

---

### 💡 Key Takeaways

- Use **SetGID** (`chmod g+s`) on shared folders so files created inside inherit the group.
- **Switch users** to confirm access works as expected.
- Permissions like `770` give the owner and group full access but block others.
- A group-shared folder ensures better collaboration and consistent ownership.

---

⏭️ **Next Up:** I’ll continue exploring user and permission management, including ACLs (Access Control Lists) and sticky bits.

