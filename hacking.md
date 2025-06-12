## Penetration Testing (PenTesting)
* Simulated cyberattack designed to identify vulnerabilities in a system's security
* Steps for penetration testing

| Step                     | Description                                                                       |
| :----------------------- | :-------------------------------------------------------------------------------- |
| **1. Planning**          | Understand the target: websites, servers, APIs, networks. Get permissions.        |
| **2. Reconnaissance**    | Gather information (like IPs, domains, emails) using tools (Google, whois, nmap). |
| **3. Scanning**          | Look for open ports, services, software versions.                                 |
| **4. Exploitation**      | Try to break in — use known exploits, phishing, weak passwords, etc.              |
| **5. Post-exploitation** | Once inside, test how deep you can go: steal data, escalate privileges.           |
| **6. Reporting**         | Document everything found, how you hacked in, and how to fix it.                  |

* Types of penetration testing:
    * Network Pen test: Servers, routers, firewalls, VPNs
    * Web Application Pen Test: Websites, APIs
    * Mobile App Pen Test: Android, iOS, etc.
    * Wireless Pen Test: Wi-Fi networks
    * Social Engineering: Human Behaviour
    * Physical Pen Test: Actual Office Break ins

## Exploit Development
* The process of finding a vulnerability in a system, understanding it deeply, and writing code (an exploit) that takes advantage of that vulnerability to control or manipulate the target.



## Reverse Shell
* A reverse shell is when the target machine connects back to the attacker's machine, giving the attacker remote command line control over it
* Most firewalls block incoming connections, but allow outgoing connections (HTTP, etc.). So, a reverse shell easily goes out through the firewall to attacker.


## Tools Used
### NMap (Network Mapper)
* It is a network scanning tool
* Helps you find devices, open ports, and services running on a network


### LOIC (Low Orbit Ion Cannon)
* Open-source network stress testing and DDoS attack tool.
* It sends a huge flood of traffic (junk HTTP requests, TCP/UDP packets) to a target server.

### Metasploit
    * Metasploit is a powerful open-source cybersecurity tool used mainly for:
        * Penetration testing (ethical hacking),
        * Exploiting vulnerabilities,
        * Developing and testing exploits,
        * Training and learning security skills.

* Pseudo Commands:
    ```
        msfconsole          # Open Metasploit Framework console
        search vsftpd       # Find an exploit for vsftpd server
        use exploit/unix/ftp/vsftpd_234_backdoor  # Load the exploit
        set RHOSTS 192.168.1.10  # Set target IP
        set LHOST 192.168.1.5    # Set your own IP
        run                  # Launch attack
    ```

### Whois



### Nikto
* Web server scanner
* It is very loud, and is only used for finding obvious web server issues
* If you run nikto on a website, they will easily see it in the logs
* Nikto is usually one of the first scans that are done, and for deeper insights, burp suite is used

### Burp Suite
* A web hacking toolkit
* Lets you intercept, modify, and attack web traffic between your browser and websites
* One of the best tools for web app penetration testing

### Wireshark
* Network packet analyzer
* Captures all the data moving on a network and lets you see it packet by packet

### John the Ripper

### Hydra
* Brute force password cracking tool. 
* Attempts to log in to services like ssh, ftp, http, and more by trying multiple passwords for a specified username

### Ghira
* A tool for reverse engineering

### IDA
* A tool for reverse engineering


### Fork Bomb
* Fork Bomb is a program that harms a system by making it run out of memory. 
* It forks processes infinitely to fill memory. The fork bomb is a form of denial-of-service (DoS) attack against a Linux based system.


### Dirb
* Dirb is a directory scanner tool that runs with a list of words (provides a default set of words) and checks if there are any vulnerabilities found on the app