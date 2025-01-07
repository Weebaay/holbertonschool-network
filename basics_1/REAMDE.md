# Networking Basics #1

## Description

This project dives deeper into the fundamentals of networking. It explores concepts such as localhost, IP addresses, and essential tools for network diagnostics and management. The tasks in this project will help you gain a better understanding of how networks function and how to interact with them effectively.

---

## Resources

### Read or Watch:
- [What is localhost](https://example.com/localhost)
- [What is 0.0.0.0](https://example.com/0.0.0.0)
- [What is the hosts file](https://example.com/hosts-file)
- [Netcat examples](https://example.com/netcat-examples)

### man or help:
- `ifconfig`
- `telnet`
- `nc`
- `cut`

---

## Learning Objectives

By the end of this project, you should be able to explain the following concepts to anyone without using Google:

### General:
- What is `localhost`/`127.0.0.1`
- What is `0.0.0.0`
- What is `/etc/hosts`
- How to display your machine’s active network interfaces

---

## Requirements

### General:
- Allowed editors: `vi`, `vim`, `emacs`
- All files will be interpreted on **Ubuntu 20.04 LTS**
- All files must end with a new line
- A `README.md` file at the root of the project folder is mandatory
- All Bash script files must be executable
- Bash scripts must pass **Shellcheck (version 0.7.0)** without errors
- The first line of all Bash scripts should be exactly `#!/usr/bin/env bash`
- The second line of all Bash scripts should be a comment explaining what the script does

---

## Tasks

### 0. Change your home IP

Write a Bash script that configures an Ubuntu server with the following requirements:

- `localhost` resolves to `127.0.0.2`
- `facebook.com` resolves to `8.8.8.8`

#### Example:
```bash
 ping localhost
PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.012 ms
^C
--- localhost ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.012/0.012/0.012/0.000 ms

 ping facebook.com
PING facebook.com (157.240.11.35) 56(84) bytes of data.
64 bytes from edge-star-mini-shv-02-lax3.facebook.com (157.240.11.35): icmp_seq=1 ttl=63 time=15.4 ms
^C
--- facebook.com ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 15.432/15.432/15.432/0.000 ms

 sudo ./0-change_your_home_IP

 ping localhost
PING localhost (127.0.0.2) 56(84) bytes of data.
64 bytes from localhost (127.0.0.2): icmp_seq=1 ttl=64 time=0.012 ms
64 bytes from localhost (127.0.0.2): icmp_seq=2 ttl=64 time=0.036 ms
^C
--- localhost ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1000ms
rtt min/avg/max/mdev = 0.012/0.024/0.036/0.012 ms

 ping facebook.com
PING facebook.com (8.8.8.8) 56(84) bytes of data.
64 bytes from facebook.com (8.8.8.8): icmp_seq=1 ttl=63 time=8.06 ms
^C
--- facebook.com ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 8.065/8.065/8.065/0.000 ms
```

**Repository:**
- GitHub repository: `holbertonschool-network`
- Directory: `basics_1`
- File: `0-change_your_home_IP`

---

### 1. Show attached IPs

Write a Bash script that displays all active IPv4 IPs on the machine it’s executed on.

#### Example:
```bash
 ./1-show_attached_IPs | cat -e
10.0.2.15$
127.0.0.1$

```

**Repository:**
- GitHub repository: `holbertonschool-network`
- Directory: `basics_1`
- File: `1-show_attached_IPs`

---

### 2. Port listening on localhost

Write a Bash script that listens on port `98` on localhost.

#### Terminal 0 (Starting the script):
```bash
 sudo ./2-port_listening_on_localhost
```

#### Terminal 1 (Connecting via `telnet`):
```bash
 telnet localhost 98
Trying 127.0.0.2...
Connected to localhost.
Escape character is '^]'.
Hello world
test
```

#### Terminal 0 (Receiving the text):
```bash
 sudo ./2-port_listening_on_localhost
Hello world
test
```

**Repository:**
- GitHub repository: `holbertonschool-network`
- Directory: `basics_1`
- File: `2-port_listening_on_localhost`

---

## Author

**DIJEONT jean-paul**
