# Day 16: Network Basics - Network Testing and Script Execution

## Overview

For Day 16, the focus was on understanding network basics in a Linux environment, including network configuration, testing connectivity, and creating a network status script to monitor network interfaces, DNS resolution, and connectivity. I used both **WSL (Windows Subsystem for Linux)** and **AWS EC2** instances for testing and troubleshooting.

### Tasks Completed:
1. Launched a VM on AWS for network testing.
2. Pulled and ran a Docker website image for dns testing.
3. Created a script to check network status and ping connectivity.
4. Troubleshot DNS lookup issues and packet loss by modifying firewall rules.

---

## Images: all in the image folder

### Image 1: Launched a VM for Network Testing
**Description**: Launched an Ubuntu VM on AWS for performing network tests and diagnostics.


### Image 2: Pulled Docker Website Image
**Description**: Pulled a Docker image for the website to simulate dns testing.


### Image 3: Ran Docker Image
**Description**: Ran the Docker image


### Image 4: Created Network Status Script
**Description**: Created a Bash script (`network_status.sh`) to check network status, including hostname, network interfaces, ping, and DNS resolution.


### Image 5: Pasted and Saved it in a File on WSL
**Description**: Pasted the script code into a file in WSL and saved it for execution.


### Image 6: Also Saved in AWS EC2 Ubuntu Terminal
**Description**: Saved the same script in an AWS EC2 instance running Ubuntu for testing in a cloud environment.


### Image 7: Made the Script Executable and Ran It in WSL
**Description**: Made the script executable with `chmod +x` and ran it inside WSL to test its functionality.


### Image 8: Made the Script Executable and Ran It in AWS EC2
**Description**: Made the script executable and ran it on the AWS EC2 Ubuntu instance.


### Image 9: Output on WSL Did Not Deliver Result on DNS Lookup as `dnsutils` was Not Installed
**Description**: The script ran but DNS lookup failed on WSL because `dnsutils` was not installed. The error message `nslookup: command not found` was displayed.


### Image 10: Output on AWS EC2
**Description**: The script successfully ran on AWS EC2, providing network interface details.


### Image 11: Output Continued on AWS EC2
**Description**: more of the output showing the network status on the EC2 instance, including DNS lookup.


### Image 12: Output Showed 100% Packet Loss, So Allowing Ping Access in Security Group
**Description**: The output showed 100% packet loss due to ping being blocked by AWS security group settings. The solution was to allow ICMP traffic in the security group.


### Image 13: Pinged the Server After Updating Firewall Rules and It Was Successful
**Description**: After updating the firewall rules, the ping test to the server was successful, indicating that ICMP traffic was now allowed.


### Image 14: Ping Working Fine
**Description**: The final successful ping test result on AWS EC2 showing no packet loss and successful round-trip times.

---

## Conclusion

By the end of Day 16, I successfully tested networking on both **WSL** and **AWS EC2**. I learned to troubleshoot network connectivity and DNS resolution issues, and modified firewall rules to allow **ICMP traffic (ping)**. The **network status script** was useful for quickly gathering information on network interfaces, DNS lookup, and connectivity.

---
