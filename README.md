#   THE BOURNE - AGAIN SHELL
## File , Directory and Access Management

| Code Snippet | Description |
| ------------ | ----------- |
| `ls`         | List the files and directories in the current directory |
| `man ls`     | Gives you more specific user guide/manual with the command `man` by giving the program name as argument |
| `cd dir/`    | Change directory to the directory named `dir` |
| `pwd`        |print working directory,In Linux the home folder of a user is usually located in `/home/user/`, and in MacOS it’s in `/Users/user/` |
| `~`          |It referes to users home directory, e.g  the Downloads folder in Linux would be either `/home/user/Downloads` or `~/Downloads` |
| `. or ..`    |Dots are often used in relative paths. `One dot .` refers to the current folder, and `two dots ..` refers to the folder the current         folder is in |
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

##  File Mods(permissions)

| Mod | Value | Shorthand |
| ------------ | ----------- |  ----------- |
| `Read`         | 4 | r |
| `Write`         | 2 | w |
| `Execute`         | 1 | x |
## Classes of users
| Shorthand | Class | Description |
| ------------ | ----------- |  ----------- |
| `u`         | Owner /user | Who own the file |
| `g`         | Group | users in the file's group |
| `o`         | Others | All other users |
| `a`         | All  | evertything above |



## Unix file system

| Code Snippet | Description |
| ------------ | ----------- |
| `/`         |Root of the file system |
| `/bin`        | Binary - containing executable programs(such as ls,cp) |
| `/dev`       | Devices - containing files represeting devices |
| `/dev/null`  | If you dont want to show the output you can send it to /dev/null, ` ls -l jfdkjfd 2>/dev/null` (2 & 1 means using the same target for both output & error streams, /dev/null is a null file) the error message will go to the null file which will descarded, ` ls -l >/dev/null` this is a correct message will go also to null file |
| `/etc`   | Containing system configurations & databases|
| `/home` |Home directory for users |
| `/lib` |Containing system libraries & device drivers |
| `/tmp` | For temprary files |
| `/usr` | Containing non system-critical libraries, executables |

## Moving and Renaming files

| Code Snippet | Description |
| ------------ | ----------- |
| `cp`         | `cp (copy)` It takes the path to the file to be copied and the target path as arguments |
| `cp example.txt example2.txt`        |copies the file example.txt as a file called example2.txt in the current folder. |
| `cp example.txt ~/Documents/example2.txt`       | copies the file `example.txt` to the Documents folder and renames it to `example2.txt` |
| `cp example.txt ~/Documents/`   | `copies` the file to Documents and keeps the name as `example.txt` |
| `mv exmple.txt example.txt` | Renames the file exmple.txt to example.txt. |
| `mv example.txt ~` | Moves the file `example.txt` from the current folder to the `home folder`.|
| `mv exmple.txt ~/example.txt` | renames the file `exmple.txt` from the `current folder to example.txt and moves it to the home folder`. |
| `mv ~/example.txt ~/Downloads/` | moves the file `example.txt` from the `home folder to the Downloads folder`. |
| `rm -r  CS2` or `rm -r -f CS2` |  would remove the directory named "CS2" and all its contents without prompting for confirmation.`-r` stands for `recursive` and will remove all directories and files within the specified directory
`-f` stands for `force` and will not prompt for confirmation before removing files or directories, It's important to use this command with caution|

## Wild Cards
### Wild cards allow one to perform operations on several files at the same time.

| Code Snippet | Description |
| ------------ | ----------- |
| `*`         | It  corresponds to any amount of any given symbol. |
| `mv *.txt example/` | moves all the files in the current directory ending with `.txt` to a folder caller `example` |
| `mv test* tests/`       | would move all the files starting with test to a folder called `tests`. |


## System Information and Management

| Code Snippet | Description |
| ------------ | ----------- |
| `ps`         | List the currently running processes |
| `top`        | Display real-time system information, including CPU usage and memory usage |
| `htop`       | Interactive process viewer, similar to `top` |
| `kill pid`   | Terminate the process with the specified process ID |
| `sudo command` | Run the specified command with administrative privileges |
| `ps -ax  \| less` | View and navigate long file |
| `ps -ax  \| grep /usr/local/bin/node \| awk {print $1}` | Print process ID (pid) of node programs|


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
| `>`  | writing outputs to files , also overwrites the contents of the file with the given text|
| `>>`  | appends the new content  to a new line, not affecting the old contents. like `>`|
| `<`  | Input Stream, or  reading from a file `  cat < java.txt ` reads text from the file|
| `wc -l countLinus.txt `  | The wc command is used to find the `number of lines, characters, words, and bytes of a file`|


## Search commands from Terminal 

| Code Snippet | Description |
| --- | --- |
| `grep pattern file_name` | Search for the specified pattern in the specified file |
| `grep -r pattern directory_name` | Search for the specified pattern in all files in the specified directory and its subdirectories |
| `grep -i  "unix" linux.txt`  | Search for "unix" text in the linux file, ignoring case |
| `grep  U* linux.txt `  | Search for text  in the linux file, that begins with uppre case `U` |
| `\|` | usually called the `pipe`. With the pipe you can do more complicated operations which require several programs with just one line. `~/example$ ls | grep note` An example of using a `pipe` is to pass the output of `ls` to `grep` in order to filter out specific filenames:|
| `grep -i  u* linux.txt > result.txt`  | Write all the outputs from left side into right side file, creating the file if it doesn’t already exist.|
| `grep -w pattern file_name` | Search for the specified word as a whole word in the specified file |
|`ps -ax \| grep /usr/local/bin/node \| awk '{print $1}' > ./pids.txt` | What this command does? |
| `find directory_path -name file_name` | Search for files with the specified name in the specified directory and its subdirectories |
| `find directory_path -type f -mtime +n` | Search for files modified more than n days ago in the specified directory and its subdirectories |
| `find directory_path -type f -size +n[cwbkMG]` | Search for files larger than n units (cwbkMG) in the specified directory and its subdirectories |
| `history` | Display the list of commands executed in the current terminal session |
| `history n` | Display the last n commands executed in the current terminal session |
| `history -c` | Clear the command history for the current terminal session |
| `history -a` | Append the commands executed in the current terminal session to the history file |
| `history -r` | Read the commands from the history file and append them to the current session history |
| `history grep pattern` | Search for commands that contain the specified pattern in the current session history |

## Bash in Vim Editor

| Code Snippet | Description |
| ------------ | ----------- |
| `#!/bin/bash`   | Its called shebang line for a Bash script, which specifies the interpreter that should be used to run the script. In this case, the shebang line                   specifies that the script should be run using the Bash interpreter. Its Always should be in  first line|
| `# This is a bash comment` |Single line comment|
| `: ' Multiple line ' ` | Multiple line comment |
| `: set nu ` | To insert code line number in Vim editor  |
| `:set nonu  `  | To remove code line number in Vim editor |
| `set nu `  |If you want to see  code line number in Vim editor Every time, NB. no colun(:) in this case |
| `chmod +x first_script.sh` | Run Bash on Terminal, always add execution Permission |

## Standard Streams
![standard Image](https://github.com/mesfint/bash-cheat-sheet/blob/main/standardStreams.png)



## Environment Variables(env)

| Code Snippet | Description |
| ------------ | ----------- |
| `env`         | It will print a list of all environment variables and their values, It also displays the current environment variables for the current shell session |
| `env less`    | Command is a text pager that allows you to view long text files or command output one page at a time. |
| ` env ` \| `grep user` |Search for user |
| `printenv or printenv HOME`   | Prints only the specified environment variable  |
| `printenv SHELL LC_TIME PWD` | prints the values accordingly |
| `set`  \| `grep HIST` | Search valriables |


##  Others

| Code Snippet | Description |
| ------------ | ----------- |
| `alias`   | Is a shortcut to a command `e.g alias server=ssh -p 2299 admin@189.24.5.6` |
|`alias alias_name=´command_to_run` | To create an alias, `nano ~/.bashrc` , eg. `alias now=date +%F\ %T, then source  ~/.bashrc`, will update the bash |

