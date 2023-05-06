#   THE BOURNE - AGAIN SHELL
## File , Directory and Access Management

| Code Snippet | Description |
| ------------ | ----------- |
| `ls`         | List the files and directories in the current directory |
| `cd dir/`    | Change directory to the directory named `dir` |
| `mkdir dir`  | Create a new directory named `dir` |
| `touch file` | Create a new empty file named `file` |
| `rm file`    | Delete the file named `file` |
| `rm -r dir`  | Delete the directory named `dir` and all its contents |
| `chmod u+rwx file_or_directory ` | To give `read`,`write`, and `execute` permissions to the owner of a file or directory |
| `chmod g+rwx file_or_directory ` | To give read, write, and execute permissions to the group associated with a file or directory: |
| `chmod a+rwx file_or_directory ` |To give read, write, and execute permissions to all users (i.e. the owner, group, and others): |
| `chmod a-x file_or_directory ` | To remove execute permission for all users from a file or directory: |
| `chmod 755 file_or_directory` | To set the permissions of a file or directory to a specific octal value, for example, 755 (rwxr-xr-x): |
| `chmod -R permissions file_or_directory`|To set the permissions of a file or directory recursively, including all files and subdirectories within it: |

## System Information and Management

| Code Snippet | Description |
| ------------ | ----------- |
| `ps`         | List the currently running processes |
| `top`        | Display real-time system information, including CPU usage and memory usage |
| `htop`       | Interactive process viewer, similar to `top` |
| `kill pid`   | Terminate the process with the specified process ID |
| `sudo command` | Run the specified command with administrative privileges |

## Shell vs Scripts

| Code Snippet | Description |
| ------------ | ----------- |
| `shell`         |Is an interface bn user and kernel |
| `bash`        |When a user login the bash starts, `bash => name of your shell` |
| `echo $0`       | To check what shell is active when a user login |
| `echo $SHELL`   | to see the default shell|
| `cat /etc/shells` | To see a list of default shells |

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

## Search commands from Terminal 

| Code Snippet | Description |
| --- | --- |
| `grep pattern file_name` | Search for the specified pattern in the specified file |
| `grep -r pattern directory_name` | Search for the specified pattern in all files in the specified directory and its subdirectories |
| `grep -i pattern file_name` | Search for the specified pattern in the specified file, ignoring case |
| `grep -w pattern file_name` | Search for the specified word as a whole word in the specified file |
| `find directory_path -name file_name` | Search for files with the specified name in the specified directory and its subdirectories |
| `find directory_path -type f -mtime +n` | Search for files modified more than n days ago in the specified directory and its subdirectories |
| `find directory_path -type f -size +n[cwbkMG]` | Search for files larger than n units (cwbkMG) in the specified directory and its subdirectories |
| `history` | Display the list of commands executed in the current terminal session |
| `history n` | Display the last n commands executed in the current terminal session |
| `history -c` | Clear the command history for the current terminal session |
| `history -a` | Append the commands executed in the current terminal session to the history file |
| `history -r` | Read the commands from the history file and append them to the current session history |
| `history` | `grep pattern` | Search for commands that contain the specified pattern in the current session history |



##  Others

| Code Snippet | Description |
| ------------ | ----------- |
| `alias`   | Is a shortcut to a command `e.g alias server=ssh -p 2299 admin@189.24.5.6` |
|`alias alias_name=´command_to_run` | To create an alias, `nano ~/.bashrc` , eg. `alias now=date +%F\ %T, then source  ~/.bashrc`, will update the bash |

