# Nmap Cheat Sheet

Nmap is a powerful open source tool for network discovery and security auditing.

Below are all Nmap commands categorised for easy reference.

## Basic Scanning

- **Scan a single target:** Performs a basic scan of a single IP or hostname.
  ```bash
  nmap <target>
  ```
- **Scan multiple targets:** Scans multiple IPs or hostnames in one command.
  ```bash
  nmap <target1> <target2>
  ```
- **Scan an entire subnet:** Scans all IPs in a specified subnet.
  ```bash
  nmap 192.168.1.0/24
  ```
- **Scan a range of IPs:** Scans a specified range of IPs.
  ```bash
  nmap 192.168.1.1-50
  ```
- **Scan a list of targets from a file:** Reads a list of targets from a file and scans them.
  ```bash
  nmap -iL targets.txt
  ```
- **Exclude hosts from a scan:** Excludes specified IPs or hosts from the scan.
  ```bash
  nmap --exclude <target>
  ```
- **Perform a no DNS resolution scan:** Avoids resolving hostnames to IPs.
  ```bash
  nmap -n <target>
  ```
- **Scan with OS fingerprinting:** Identifies the OS of the target.
  ```bash
  nmap -O <target>
  ```

## Port Scanning

- **Scan all 65535 ports:** Checks every possible port on a target.
  ```bash
  nmap -p 1-65535 <target>
  ```
- **Scan top 1000 common ports:** Checks for the most frequently used ports.
  ```bash
  nmap -F <target>
  ```
- **Scan only open ports:** Displays only ports that are open.
  ```bash
  nmap --open <target>
  ```
- **Scan UDP ports:** Scans for open UDP ports instead of TCP.
  ```bash
  nmap -sU <target>
  ```
- **Scan using TCP SYN packets:** Performs a stealth scan without full connection.
  ```bash
  nmap -sS <target>
  ```
- **Scan using TCP connect:** Establishes a full connection to check port status.
  ```bash
  nmap -sT <target>
  ```

## Service and OS Detection

- **Detect service versions:** Identifies the version of running services.
  ```bash
  nmap -sV <target>
  ```
- **Aggressive scan:** Performs OS detection, version detection, script scanning, and traceroute.
  ```bash
  nmap -A <target>
  ```
- **Detect RPC services:** Scans for remote procedure call (RPC) services.
  ```bash
  nmap -sR <target>
  ```

## Firewall and IDS Evasion

- **Scan with decoys:** Disguises the scan by using multiple decoy IPs.
  ```bash
  nmap -D RND:10 <target>
  ```
- **Use a specific TTL:** Sets a custom time-to-live value.
  ```bash
  nmap --ttl 64 <target>
  ```
- **Send packets with invalid checksums:** Used for firewall evasion.
  ```bash
  nmap --badsum <target>
  ```
- **Use random scanning order:** Scans targets in a random order.
  ```bash
  nmap --randomize-hosts <target>
  ```

## Script Scanning

- **Run all available scripts:** Uses all NSE scripts.
  ```bash
  nmap --script all <target>
  ```
- **Run scripts for a specific vulnerability:**
  ```bash
  nmap --script http-vuln-cve2017-5638 <target>
  ```
- **Run brute-force scripts:**
  ```bash
  nmap --script brute <target>
  ```
- **Run scripts for malware detection:**
  ```bash
  nmap --script malware <target>
  ```

## Output and Reporting

- **Save output in all formats:** Saves output in normal, XML, and grepable formats.
  ```bash
  nmap -oA output <target>
  ```
- **Append scan results to an existing file:**
  ```bash
  nmap -oN output.txt --append-output <target>
  ```
- **Output only IP addresses:** Displays only IPs of discovered hosts.
  ```bash
  nmap -sP --open <target>
  ```

## Performance and Timing

- **Scan at maximum speed:** Uses the fastest scan setting.
  ```bash
  nmap -T5 <target>
  ```
- **Slow scan for stealth:** Reduces scanning speed for less detection.
  ```bash
  nmap -T1 <target>
  ```
- **Minimize scan retries:** Reduces the number of retries for faster scans.
  ```bash
  nmap --max-retries 2 <target>
  ```

## Advanced Techniques

- **Use IPv6 scanning:** Enables scanning of IPv6 addresses.
  ```bash
  nmap -6 <target>
  ```
- **Traceroute to a target:** Determines the route packets take.
  ```bash
  nmap --traceroute <target>
  ```
- **Detect live hosts only (ping scan):**
  ```bash
  nmap -sn <target>
  ```
- **Use a spoofed source IP:**
  ```bash
  nmap -S <fake-ip> <target>
  ```
- **Adjust the scan delay between packets:**
  ```bash
  nmap --scan-delay 5s <target>
  ```
- **Scan specific Ethernet interface:**
  ```bash
  nmap -e eth0 <target>
  ```
- **Scan a specific DNS server for resolution:**
  ```bash
  nmap --dns-servers 8.8.8.8 <target>
  ```

## Conclusion

This cheat sheet includes nearly every Nmap command available, providing a complete reference for scanning, reconnaissance, and penetration testing. Explore more options with:
```bash
man nmap
```
