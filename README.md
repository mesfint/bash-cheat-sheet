## File and Directory Management

| Code Snippet | Description |
| ------------ | ----------- |
| `ls`         | List the files and directories in the current directory |
| `cd dir/`    | Change directory to the directory named `dir` |
| `mkdir dir`  | Create a new directory named `dir` |
| `touch file` | Create a new empty file named `file` |
| `rm file`    | Delete the file named `file` |
| `rm -r dir`  | Delete the directory named `dir` and all its contents |

## System Information and Management

| Code Snippet | Description |
| ------------ | ----------- |
| `ps`         | List the currently running processes |
| `top`        | Display real-time system information, including CPU usage and memory usage |
| `htop`       | Interactive process viewer, similar to `top` |
| `kill pid`   | Terminate the process with the specified process ID |
| `sudo command` | Run the specified command with administrative privileges |


## Commonly Used Bash Commands for Network Management

|  Code Snippet | Description |
| --- | --- |
| `ping [address]` | Sends an ICMP echo request to a specific network address to test network connectivity. |
| `traceroute [address]` | Displays the path that packets take to reach a network address, along with the time taken by each hop. |
| `netstat` | Displays active network connections, routing tables, and related network statistics. |
| `netstat -tupan` | Display all the active TCP and UDP connections on your system along with the associated process or program name, IP address, and port number. |
| `ifconfig` | Displays the configuration of network interfaces, including IP addresses and network masks. |
| `route` | Displays and modifies the routing table of the network stack. |
| `arp` | Displays and modifies the ARP cache, which maps network addresses to physical addresses. |
| `ssh [user@]host` | Connects to a remote host over the network using the SSH protocol. |
| `scp [options] [source] [destination]` | Copies files securely between hosts over the network using the SSH protocol. |
| `wget [URL]` | Downloads files from the network using HTTP, HTTPS, or FTP protocols. |
| `curl [options] [URL]` | Downloads or uploads data to or from the network using various protocols, including HTTP, HTTPS, FTP, and SCP. |


## Text Processing and Manipulation

| Code Snippet | Description |
| ------------ | ----------- |
| `cat file`   | Display the contents of the file named `file` |
| `grep pattern file` | Search for lines in the file named `file` that match the specified `pattern` |
| `sed 's/old/new/g' file` | Replace all occurrences of `old` with `new` in the file named `file` |
| `awk '{print $1}' file` | Print the first field of each line in the file named `file` |
| `cut -d',' -f1 file` | Extract the first column of a CSV file named `file` |

##  Others

| Code Snippet | Description |
| ------------ | ----------- |
| `alias`   | Is a shortcut to a command `e.g alias server=ssh -p 2299 admin@189.24.5.6` |
|`alias alias_name=´command_to_run` | To create an alias, `nano ~/.bashrc` , eg. `alias now=date +%F\ %T, then source  ~/.bashrc`, will update the bash |

