# 📁 Day 10: User Account Management & Shell Access Control

Today’s focus was on **user login control**, **password management**, and **account restrictions**. I explored how to list users who can log into the shell, created new users with specific roles, and tested login permissions by enabling and disabling shell access.

---

## 🔧 Summary of Skills Practiced

- Checked users with shell access via `/etc/passwd`
- Created new users (`developer1`, `audituser`)
- Set password and account expiry date
- Locked user account to prevent login (`passwd -l`)
- Forced password reset and viewed expiry info
- Verified shell access restrictions

> ✅ *This session helped solidify my understanding of how Linux manages user login permissions and security controls. I now understand how to secure accounts that shouldn't have direct shell access.*

---

## 📸 Screenshots of Practice

1. ✅ Checked existing users that can log into the shell and created a new user `developer1`  
2. ✅ Added `audituser` and verified the user’s login shell  
3. ✅ Locked `audituser` to restrict shell login, and set password for `developer1`  
4. ✅ Viewed password expiry details for `developer1` and forced a password reset  
5. ✅ Confirmed that `audituser` could not log in to the shell  

---

## 💡 Key Commands & Concepts

- View users and their login shells:  
  `cat /etc/passwd | grep "/bin/bash"`


- Lock a user account (disable login):  
  `sudo passwd -l audituser`

- Set a password and force reset at next login:  
  ```bash
  sudo passwd developer1
  sudo chage -d 0 developer1

- View password ageing information:
  sudo chage -l developer1