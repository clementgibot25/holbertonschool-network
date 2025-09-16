# Networking Basics

## OSI Model

### What is the OSI Model?
The OSI (Open Systems Interconnection) Model is a conceptual framework used to understand and standardize the functions of a telecommunication or computing system without regard to its underlying internal structure and technology.

### Layers of the OSI Model
1. **Physical Layer (Layer 1)**: Deals with the physical connection between devices and raw bit stream transmission.
2. **Data Link Layer (Layer 2)**: Handles node-to-node data transfer and error detection/correction.
3. **Network Layer (Layer 3)**: Manages device addressing, tracks device locations, and determines the best path for data transfer.
4. **Transport Layer (Layer 4)**: Ensures complete data transfer and error checking.
5. **Session Layer (Layer 5)**: Establishes, manages, and terminates connections between applications.
6. **Presentation Layer (Layer 6)**: Translates data between the application and network formats.
7. **Application Layer (Layer 7)**: Provides network services directly to end-user applications.

## Network Types

### Local Area Network (LAN)
- **Definition**: A network that connects devices within a limited area such as a home, school, or office building.
- **Typical Usage**: Sharing resources like files, printers, and internet connections among devices in close proximity.
- **Geographical Size**: Typically spans a few kilometers at most.

### Wide Area Network (WAN)
- **Definition**: A network that covers a broad area (any network that crosses metropolitan, regional, or national boundaries).
- **Typical Usage**: Connecting multiple LANs across large distances, often used by businesses with multiple locations.
- **Geographical Size**: Can span across cities, countries, or even globally.

### The Internet
- The Internet is a global network of interconnected computer networks that uses the Internet Protocol Suite (TCP/IP) to communicate between networks and devices.
- It's essentially a network of networks that consists of millions of private, public, academic, business, and government networks.

## IP Addressing

### What is an IP Address?
An Internet Protocol (IP) address is a numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication.

### Types of IP Addresses
1. **IPv4**: 32-bit address (e.g., 192.168.1.1)
   - Most widely used version
   - Limited to about 4.3 billion unique addresses

2. **IPv6**: 128-bit address (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334)
   - Created to replace IPv4 due to address exhaustion
   - Provides approximately 3.4×10^38 unique addresses

### Localhost
- A hostname that refers to the current device used to access it.
- The IP address for localhost is typically `127.0.0.1` (IPv4) or `::1` (IPv6).
- Used to access network services running on the host via the loopback network interface.

### Subnet
- A logical subdivision of an IP network.
- Allows for better organization, improved security, and more efficient routing of network traffic.
- Example: `192.168.1.0/24` is a common subnet mask for home networks.

### Why IPv6 was Created
- IPv6 was developed to deal with IPv4 address exhaustion.
- Provides a much larger address space than IPv4.
- Includes improvements in routing and network autoconfiguration.
- Better support for mobile devices and security features.

## Transport Layer Protocols

### TCP (Transmission Control Protocol)
- Connection-oriented protocol.
- Reliable, ordered, and error-checked delivery of data.
- Slower than UDP due to overhead.
- Used for web browsing (HTTP/HTTPS), email (SMTP), and file transfers (FTP).

### UDP (User Datagram Protocol)
- Connectionless protocol.
- Faster than TCP but less reliable (no guaranteed delivery).
- No error correction.
- Used for video streaming, online gaming, and VoIP.

## Ports
- Virtual points where network connections start and end.
- Identified by port numbers (0-65535).
- Common port numbers to remember:
  - **SSH**: 22
  - **HTTP**: 80
  - **HTTPS**: 443
  - **FTP**: 21
  - **DNS**: 53

## Network Diagnostics
- **Ping**: A network administration utility used to test the reachability of a host on an IP network.
  - Example: `ping google.com`
  - Uses ICMP (Internet Control Message Protocol)

- **Traceroute/tracert**: Shows the path that a packet takes to reach a destination.
  - Useful for diagnosing network routing issues.

- **netstat**: Displays network connections, routing tables, and interface statistics.
  - Useful for monitoring network connections and troubleshooting.

## Common Network Tools
1. **Ping**: Tests connectivity between two network devices.
2. **Traceroute/tracert**: Maps the path data takes to reach a destination.
3. **netstat**: Displays network connections and listening ports.
4. **nslookup/dig**: Queries DNS to obtain domain name or IP address mapping.
5. **ipconfig/ifconfig**: Displays network configuration.
6. **tcpdump/Wireshark**: Packet sniffers for network analysis.

## Security Considerations
- **Firewalls**: Control incoming and outgoing network traffic.
- **VPNs**: Create secure connections over the internet.
- **HTTPS**: Encrypts web traffic.
- **SSH**: Secure remote access to systems.
- **SFTP/SCP**: Secure file transfer protocols.