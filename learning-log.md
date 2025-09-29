# Essential Commands

- `ls` - list files and directories
- `cd` - change directory
- `cat` - display file contents
- `file` - determine file type
- `find` - search for files
- `grep` - search text patterns
- `sort` - sort lines of text
- `uniq` - remove duplicate lines
- `strings` - extract readable strings from files
- `base64` - encode/decode base64
- `tr` - translate characters
- `tar` - archive files
- `gzip` - compress files
- `xxd` - hex dump utility

# Useful Tools
##### Networking & Connection Tools
- `openssh-client`: Your main tool for connecting to Bandit levels
- `telnet`: Used for plain-text connections and protocol testing
- `netcat-openbsd`: Swiss army knife for network connections
- `curl/wget`: Download files and interact with web services
##### Text Editors & System Utilities
- `vim/nano`: Edit files and scripts
- `htop`: Monitor system processes
- `tree`: Visualize directory structures
##### Security & Analysis Tools
- `nmap`: Port scanning and service detection
- `wireshark`: GUI network protocol analyzer
- `tcpdump`: Command-line packet capture
##### Binary & Data Analysis
- `hexedit`: Interactive hex editor
- `xxd`: Hex dump utility
- `binutils`: Collection of binary utilities
##### Development Tools
- `git`: Clone repositories and manage code
- `python3`: Scripting and automation
- `gcc/make`: Compile C programs

# Tools Overview

##### Netcat
- Often called the "Swiss-army knife" for networking, is a command-line utility used to read from and write to network connections using TCP or UDP.
- At its most basic, `nc` can operate in two modes:
	- **Client Mode**: In this mode, `nc` connects to a listening server on a specified host and port.
	- **Listen Mode**: Here, `nc` binds to a specific port and waits for incoming connections, effectively turning your machine into a simple server.

# Concepts

##### Secure Shell Protocol (SSH Protocol)
- The **Secure Shell Protocol (SSH Protocol)** is a cryptographic network protocol for operating network services securely over an unsecured network. Its most notable applications are remote login and command-line execution.
- SSH was designed for Unix-like operating systems as a replacement for Telnet and unsecured remote Unix shell protocols, such as the Berkeley Remote Shell (rsh) and the related rlogin and rexec protocols, which all use insecure, plaintext methods of authentication, such as passwords.
- Since mechanisms like Telnet and Remote Shell are designed to access and operate remote computers, sending the authentication tokens (e.g. username and password) for this access to these computers across a public network in an unsecured way poses a great risk of third parties obtaining the password and achieving the same level of access to the remote system as the telnet user. Secure Shell mitigates this risk through the use of encryption mechanisms that are intended to hide the contents of the transmission from an observer, even if the observer has access to the entire data stream.
> https://en.wikipedia.org/wiki/Secure_Shell

##### ROT13
- **ROT13** is a simple letter substitution cipher that replaces a letter with the 13th letter after it in the Latin alphabet.
- Using `tr` for ROT13 on Linux:
	- `tr 'A-Za-z' 'N-ZA-Mn-za-m'`

##### Hex Dump
- In computing, a **hex dump** is a textual hexadecimal view (on screen or paper) of computer data, from memory or from a computer file or storage device. Use of a hex dump of data is usually done in the context of either debugging, reverse engineering or digital forensics.
- In a **hex dump**, each byte (8 bits) is represented as a two-digit hexadecimal number. Hex dumps are commonly organized into rows of 8 or 16 bytes, sometimes separated by whitespaces. Some hex dumps have the hexadecimal memory address at the beginning. On systems where the conventional representation of data is octal, the equivalent is an octal dump.

##### Localhost
- In computer networking, localhost is a hostname that refers to the current computer used to access it. The name localhost is reserved for loopback purposes. It is used to access the network services that are running on the host via the loopback network interface. Using the loopback interface bypasses any local network interface hardware.
- The local loopback mechanism may be used to run a network service on a host without requiring a physical network interface, or without making the service accessible from the networks the computer may be connected to. For example, a locally installed website may be accessed from a Web browser by the URL http://localhost to display its home page.

##### Ports
- In computer networking, a port is a communication endpoint. At the software level within an operating system, a port is a logical construct that identifies a specific process or a type of network service. A port is uniquely identified by a number, the port number, associated with the combination of a transport protocol and the network IP address. Port numbers are 16-bit unsigned integers.
- The most common transport protocols that use port numbers are the **Transmission Control Protocol (TCP)** and the **User Datagram Protocol (UDP)**. The port completes the destination and origination addresses of a message within a host to point to an operating system process. Specific port numbers are reserved to identify specific services so that an arriving packet can be easily forwarded to a running application. For this purpose, port numbers lower than 1024 identify the historically most commonly used services and are called the well-known port numbers. Higher-numbered ports are available for general use by applications and are known as ephemeral ports.



