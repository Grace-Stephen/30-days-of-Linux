# 🧠 Day 18 - Linux Services Management with `systemctl` 

## 📌 Objective
Practice and understand how to manage services on a Linux system using `systemctl` commands. Also, simulate, debug, and fix service-related issues in a real-world scenario using Apache2.

---

## 🧰 Tools & Commands Practiced

- `systemctl status`
- `systemctl start`, `stop`, `restart`, `enable`
- `systemctl list-units --type=service`
- `journalctl -xe`
- Apache2 installation & config testing

---

## 🧪 Activities & Screenshots: all in the image folder

1. ✅ **Confirmed my system uses systemd**
   - `ps -p 1 -o comm=`
   - 📸 *Screenshot:* `1 confirmed my system uses systemd.png`

2. ✅ **Viewed list of active services**
   - `systemctl list-units --type=service`
   - 📸 `2 viewed list of active services with systemctl.png`

3. ✅ **Checked status of two services (ssh and wsl)**
   - `systemctl status ssh`
   - 📸 `3 checked the status of two services - ssh and wsl.png`

4. ✅ **Viewed all services (including inactive)**
   - `systemctl list-units --type=service --all`
   - 📸 `4 viewed a list of all services including inactive ones.png`

5. ✅ **Installed Apache2 for practical testing**
   - `sudo apt install apache2`
   - 📸 `5 installed apache2 for better practice.png`

6. ✅ **Checked Apache2 service status**
   - `systemctl status apache2`
   - 📸 `6 checked the status of apache2 which showed active.png`

7. ✅ **Stopped Apache2 and verified it's inactive**
   - `sudo systemctl stop apache2`
   - 📸 `7 stopped apache2 and viewed status which now showed inactive.png`

8. ✅ **Started Apache2 again and verified it is running**
   - `sudo systemctl start apache2`
   - 📸 `8 started it again and verified it is running.png`

9. ✅ **Enabled Apache2 to start on boot**
   - `sudo systemctl enable apache2`
   - 📸 `9 enabled it at boot.png`

10. ✅ **Simulated an error by corrupting config**
    - Edited `/etc/apache2/apache2.conf` and added gibberish
    - 📸 `10 simulated an error by adding gibberish in the apache2 config.png`

11. ✅ **Tried restarting Apache2 – it failed**
    - `sudo systemctl restart apache2`
    - 📸 `11 tried to restart apache2 and it failed and status now showed inactive.png`

12. ✅ **Viewed detailed error logs**
    - `journalctl -xe`
    - 📸 `12 also checked the log with journalctl -xe.png`

13. ✅ **Fixed the config error and successfully restarted Apache2**
    - 📸 `13 fixed the error and restarted apache2 - status now shows active.png`

14. ✅ **Confirmed Apache2 is running via browser**
    - Accessed: `http://localhost`
    - 📸 `14 confirm apache2 is running in wsl via browser.png`

---

## 🧠 Key Takeaways

- Learned to start, stop, restart, and enable services using `systemctl`
- Understood how to check service status and debug errors
- Practiced simulating and fixing config-level issues in real-time
- Successfully hosted and accessed Apache2 through a browser from WSL2 using `localhost`

---

## ✅ Commands Reference

```bash
# Check systemd
ps -p 1 -o comm=

# View services
systemctl list-units --type=service
systemctl list-units --type=service --all

# Check service status
systemctl status <service-name>

# Manage services
sudo systemctl start <service>
sudo systemctl stop <service>
sudo systemctl restart <service>
sudo systemctl enable <service>

# View logs
journalctl -xe
