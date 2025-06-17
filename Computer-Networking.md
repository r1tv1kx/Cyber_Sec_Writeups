
# Computer Networking

## IP - Internet Protocol

| IP Version | Address Length | Total Addresses |
|------------|---------------|-----------------|
| IPv4       | 32 bits (4 bytes) | ~4.7 billion |
| IPv6       | 128 bits | ~340 trillion |

### Types of IP Addresses
- **Public:** Used in WAN
- **Private:** Used in LAN
- **Static:** Fixed address
- **Dynamic:** Assigned by DHCP

## TCP Flags

| Flag | Meaning |
|------|---------|
| **URG** | Urgent data in the packet should be processed immediately |
| **FIN** | No further transmission |
| **RST** | Resets a connection |
| **PSH** | Sends all buffered data immediately |
| **ACK** | Acknowledges the receipt of a packet |
| **SYN** | Initiates a connection between hosts |

## TCP 3-Way Handshake
```
A  --------> SYN -------->  B
A  <--- SYN + ACK ---- B
A  --------> ACK -------->  B
```

### Session Termination
```
First FIN  ---->  Second ACK  ---->  Third FIN  ---->  Fourth ACK
```

## TCP vs UDP

| Feature | TCP | UDP |
|---------|-----|-----|
| Connection-Oriented | Yes | No |
| Reliable | Yes | No |
| Speed | Slower | Faster |
| Example Use | Web Browsing, Email | Streaming, VoIP |

## Working of a Router
Routers direct data packets between networks based on IP addresses.

## IP Allotment Methods
- **Manual**
- **Automation:** DHCP, ARP

## Types of HTTP Requests

| Request Type | Description |
|-------------|-------------|
| **GET** | Transfers data via URL, visible and not secure |
| **POST** | Sends user info/files in the request body |
| **PUT** | Replaces all current representations of the target resource |
| **DELETE** | Removes representations of the target resource |
| **OPTIONS** | Describes available communication options |
| **TRACE** | Performs a message loopback test |
| **CONNECT** | Establishes a tunnel to a server |

## Other Concepts
- **Zone File**: A file that contains DNS information about domains and their corresponding IP addresses.
- **TCP/IP Model**: A networking model with four layers: Application, Transport, Internet, and Network Interface.
- **OSI Model**: A conceptual framework for networking that consists of seven layers (Physical, Data Link, Network, Transport, Session, Presentation, and Application).
- **Basic Linux File System**: A hierarchical structure where directories serve different purposes in system management and storage.

## DNS Records

| Record Type | Purpose |
|------------|---------|
| **A** | Maps a domain to an IPv4 address |
| **AAAA** | Maps a domain to an IPv6 address |
| **CNAME** | Alias for another domain name |
| **MX** | Mail exchange record for email routing |
| **TXT** | Stores arbitrary text, often used for verification |
| **NS** | Specifies name servers for a domain |
| **PTR** | Reverse lookup for IP to domain mapping |
| **SOA** | Start of Authority, provides administrative information about the domain |
| **SRV** | Defines location (hostname and port) of servers |
| **CAA** | Certification Authority Authorization, specifies allowed SSL certificate issuers |
| **NAPTR** | Naming Authority Pointer, used for dynamic DNS resolution |
| **DNAME** | Alias for an entire domain instead of a single record |
| **HINFO** | Host information record (CPU and OS details) |

## Layers of the Internet
The Internet consists of multiple layers, each handling different aspects of communication.

| Layer | Function |
|-------|----------|
| **Application Layer** | Provides network services to applications (HTTP, FTP, DNS) |
| **Transport Layer** | Ensures end-to-end communication (TCP, UDP) |
| **Internet Layer** | Handles addressing and routing (IP, ICMP) |
| **Link Layer** | Manages physical network transmission (Ethernet, Wi-Fi) |
| **Physical Layer** | Converts data into electrical, radio, or optical signals |

### Web Layers

| Web Layer | Description |
|-----------|-------------|
| **Surface Web** | The publicly accessible part of the internet, indexed by search engines like Google and Bing. |
| **Deep Web** | Contains content that is not indexed by search engines, including private databases, academic journals, and internal websites. |
| **Dark Web** | A part of the internet that requires specialized software like Tor to access. It is often used for anonymous communication and may include illicit activities. |
