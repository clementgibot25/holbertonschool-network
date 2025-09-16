# Network Basics - Localhost and Network Interfaces

## What is localhost/127.0.0.1?

`localhost` is a hostname that refers to the current device used to access it. The name resolves to the IP address `127.0.0.1` in IPv4 or `::1` in IPv6.

- **Purpose**: It's used to access network services running on the host via the loopback network interface.
- **Key Points**:
  - Always points back to your own computer
  - Used for testing and development
  - Bypasses network interface hardware
  - Commonly used for local web servers, databases, and other network services

## What is 0.0.0.0?

`0.0.0.0` is a special IP address with several meanings:

1. **Non-routable meta-address**: Used to designate an invalid, unknown, or non-applicable target
2. **Default route**: Represents all IPv4 addresses on the local machine
3. **In server configurations**: Means "listen on all available network interfaces"

## What is /etc/hosts?

`/etc/hosts` is a plain text file that maps hostnames to IP addresses. It's one of several system facilities that assists in addressing network nodes in a computer network.

- **Location**: `/etc/hosts` (Linux/macOS) or `C:\Windows\System32\drivers\etc\hosts` (Windows)
- **Format**: Each line contains an IP address followed by one or more hostnames
- **Uses**:
  - Local hostname resolution
  - Blocking websites
  - Testing websites before DNS propagation
  - Development environment setup

## How to Display Active Network Interfaces

### On Linux/macOS:
```bash
ifconfig
# or the newer alternative
ip a
# or for brief information
ip -br a
```

### On Windows:
```cmd
ipconfig
# or for more detailed information
ipconfig /all
```

### Using PowerShell:
```powershell
Get-NetIPConfiguration
# or for just the active interfaces
Get-NetIPInterface | Where-Object {$_.ConnectionState -eq "Connected"}
```

These commands will show you all active network interfaces along with their IP addresses, netmasks, and other relevant network information.
