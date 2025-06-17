
## What is a Port?

A port is like a door for data to enter and leave a computer, helping different services on a network communicate. Think of an IP address as a house, and ports as different doors for specific services.

Every port has a unique number (0-65535), allowing computers to send data to the right place. Ports are used in TCP and UDP protocols and help manage multiple services on the same IP address.

Example: Visiting 192.168.1.1:80 loads a website, while 192.168.1.1:22 connects securely to a remote system.

Real-world Analogy: A computer is like an apartment building, with each apartment (port) assigned to a specific service, such as mail delivery (email) or security (remote login). When data arrives, the computer directs it to the right port.

## Types of Ports

- **Well-Known Ports (0-1023):** Used by important services like websites and emails.
- **Registered Ports (1024-49151):** Used by specific applications like databases.
- **Dynamic/Private Ports (49152-65535):** Used temporarily by software or private connections.

## Common Ports and Their Uses

| Port Number  | Service           | Usage                                       |
|-------------|-------------------|---------------------------------------------|
| 20, 21      | FTP               | File transfers                              |
| 22          | SSH               | Secure remote login                         |
| 23          | Telnet            | Remote login (not secure)                   |
| 25          | SMTP              | Sending emails                              |
| 53          | DNS               | Converts website names to IPs               |
| 67, 68      | DHCP              | Assigns IP addresses                        |
| 80          | HTTP              | Websites (not secure)                       |
| 110         | POP3              | Receiving emails                            |
| 123         | NTP               | Syncing time                                |
| 135         | RPC               | Microsoft Remote Procedure Call            |
| 137-139     | NetBIOS           | Windows file sharing                        |
| 143         | IMAP              | Receiving emails (better than POP3)         |
| 161, 162    | SNMP              | Network monitoring                          |
| 389         | LDAP              | Directory services (e.g., Active Directory) |
| 443         | HTTPS             | Secure websites                             |
| 445         | SMB               | Windows file sharing                        |
| 465, 587    | SMTP              | Secure email sending                        |
| 993         | IMAPS             | Secure email receiving                      |
| 995         | POP3S             | Secure POP3 email                           |
| 1433, 1434  | SQL Server        | Microsoft database                          |
| 1521        | Oracle            | Oracle database                             |
| 3306        | MySQL             | MySQL database                              |
| 3307        | MySQL Cluster     | MySQL database clustering                   |
| 3389        | RDP               | Remote Desktop                              |
| 5353        | mDNS              | Multicast DNS (local network discovery)     |
| 5900        | VNC               | Remote access                               |
| 8080        | HTTP Alt          | Alternative web traffic                     |
| 8443        | HTTPS Alt         | Secure web traffic alternative              |
| 1812, 1813  | RADIUS            | Authentication for networks                 |
| 5060, 5061  | SIP               | Voice calls over the internet (VoIP)        |
| 1723        | PPTP              | VPN connection                              |
| 2049        | NFS               | File sharing between computers              |
| 25565       | Minecraft Server  | Multiplayer gaming server (Minecraft)      |
| 5432        | PostgreSQL        | PostgreSQL database                         |
| 5985, 5986  | WinRM             | Remote management for Windows               |
| 6379        | Redis             | Fast database/cache                         |
| 9000        | PHP-FPM           | Running PHP applications                    |
| 9200        | Elasticsearch     | Search engine service                       |
| 11211       | Memcached         | High-performance caching system             |

For more reference, visit: [List of TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)

## How to Scan Ports with Nmap

Nmap (Network Mapper) is a powerful tool used for scanning networks and identifying open ports on a target system. It helps administrators detect vulnerabilities, monitor network security, and troubleshoot connectivity issues.

#### Basic Nmap Scans:
- **Scan common ports:** `nmap <target>`  
  _This scans the most frequently used ports on a system._
- **Scan all ports (0-65535):** `nmap -p- <target>`  
  _This provides a comprehensive scan of all possible ports._
- **Find out what services are running:** `nmap -sV <target>`  
  _Detects software versions running on open ports._
- **Check for security issues:** `nmap --script vuln <target>`  
  _Uses vulnerability detection scripts to identify weaknesses._
- **Detect operating system:** `nmap -O <target>`  
  _Attempts to determine the OS of the target device._

#### Advanced Scans:
- **Aggressive scan (detailed information):** `nmap -A <target>`  
  _Combines OS detection, service version detection, script scanning, and traceroute._
- **Scan a specific port range:** `nmap -p 20-100 <target>`  
  _Focuses on a particular range of ports._
- **Stealth scan (avoiding detection):** `nmap -sS <target>`  
  _Performs a SYN scan that is less likely to be logged by firewalls._
- **Scan multiple targets:** `nmap <target1> <target2>` or `nmap -iL targets.txt`  
  _Scans multiple IP addresses or a list of targets from a file._

#### Example:
To scan a web server (e.g., `192.168.1.1`) for open ports and services, use:
```
nmap -sV -p 22,80,443 192.168.1.1
```
This will check if SSH, HTTP, and HTTPS are open and identify the software versions running on those ports.

## How to Secure Open Ports

- Close ports that are not needed.
- Use a firewall to control access.
- Encrypt data using SSH, TLS, and HTTPS.
- Use port knocking to hide important services.

Security Note: Open ports can be exploited by hackers. If unnecessary ports are open, attackers can use them to access sensitive data or take control of a system. Always monitor and secure your network.

## Conclusion

Ports are essential for communication between computers and services. Keeping track of open ports and securing them is important for a safe and efficient network. Regular scanning and monitoring help prevent security threats.
