## **Bash Built-in Commands**
*(No external process execution; part of Bash itself)*

| Command | Description |
|---------|-------------|
| `:` | No-op (do nothing, always returns true) |
| `.` | Source a file (execute in current shell) |
| `alias` | Create, list, or remove command aliases |
| `bg` | Resume a job in the background |
| `bind` | Bind a key sequence to a command or macro |
| `break` | Exit from a `for`, `while`, or `until` loop |
| `builtin` | Execute a shell built-in (bypassing aliases/functions) |
| `case` | Conditional execution based on pattern matching |
| `cd` | Change directory |
| `command` | Execute a command (bypassing aliases/functions) |
| `compgen` | Generate possible completion matches |
| `complete` | Define how argument completion is performed |
| `continue` | Resume the next iteration of a loop |
| `declare` | Declare variables and set attributes |
| `dirs` | Display directory stack |
| `disown` | Remove a job from the shell's job table |
| `echo` | Print arguments to stdout |
| `enable` | Enable/disable shell built-ins |
| `eval` | Evaluate arguments as a shell command |
| `exec` | Replace the shell process with a command |
| `exit` | Exit the shell |
| `export` | Set environment variables for child processes |
| `false` | Return a non-zero (false) exit status |
| `fc` | Fix command (edit and re-execute history) |
| `fg` | Bring a job to the foreground |
| `for` | Loop construct |
| `getopts` | Parse command-line options |
| `hash` | Remember or list command locations |
| `help` | Display help for shell built-ins |
| `history` | Manage command history |
| `if` | Conditional execution |
| `jobs` | List active jobs |
| `kill` | Send signals to processes or jobs |
| `let` | Perform arithmetic evaluation |
| `local` | Declare local variables in functions |
| `logout` | Exit a login shell |
| `popd` | Pop the directory stack |
| `printf` | Format and print arguments |
| `pushd` | Push a directory onto the stack |
| `pwd` | Print the current working directory |
| `read` | Read input from stdin into variables |
| `readonly` | Mark variables as read-only |
| `return` | Exit a function with a return value |
| `set` | Set or display shell options/variables |
| `shift` | Shift positional parameters |
| `shopt` | Set or display shell options |
| `source` | Source a file (same as `.`) |
| `suspend` | Suspend the shell |
| `test` / `[` | Evaluate conditional expressions |
| `times` | Print shell and child process times |
| `trap` | Catch and handle signals |
| `true` | Return a zero (true) exit status |
| `type` | Display information about command type |
| `typeset` | Declare variables and set attributes (same as `declare`) |
| `ulimit` | Set or display resource limits |
| `umask` | Set or display the file mode creation mask |
| `unalias` | Remove an alias |
| `unset` | Remove variables or functions |
| `until` | Loop construct (execute until condition is true) |
| `wait` | Wait for background jobs to complete |
| `while` | Loop construct (execute while condition is true) |

---

---

## **File and Directory Operations**

| Command | Description |
|---------|-------------|
| `cat` | Concatenate and display file contents |
| `chmod` | Change file permissions |
| `chown` | Change file ownership |
| `chgrp` | Change file group ownership |
| `cksum` | Print CRC checksum and byte count |
| `cp` | Copy files and directories |
| `dd` | Convert and copy a file (low-level block operations) |
| `df` | Display filesystem disk space usage |
| `du` | Estimate file space usage |
| `file` | Determine file type |
| `find` | Search for files in a directory hierarchy |
| `ln` | Create links to files |
| `ls` | List directory contents |
| `mkdir` | Create directories |
| `mkfifo` | Create FIFO (named pipe) |
| `mknod` | Create a special file (block/character device) |
| `mv` | Move or rename files |
| `od` | Dump files in octal, hexadecimal, or other formats |
| `paste` | Merge lines of files |
| `rm` | Remove files or directories |
| `rmdir` | Remove empty directories |
| `shred` | Securely delete a file |
| `touch` | Change file timestamps |
| `truncate` | Truncate or extend files to a specified size |
| `vdir` | Verbose directory listing (same as `ls -l`) |

---

---

## **Text Processing and Manipulation**

| Command | Description |
|---------|-------------|
| `awk` | Pattern scanning and processing language |
| `base64` | Encode/decode base64 data |
| `col` | Filter reverse line feeds from input |
| `column` | Format input into multiple columns |
| `comm` | Compare two sorted files line by line |
| `csplit` | Split a file into sections determined by context lines |
| `cut` | Remove sections from each line of files |
| `diff` | Compare files line by line |
| `diff3` | Compare three files line by line |
| `ed` | Line-oriented text editor |
| `ex` | Line-oriented text editor (extended `ed`) |
| `expand` | Convert tabs to spaces |
| `fmt` | Simple optimal text formatter |
| `fold` | Wrap each line to a specified width |
| `grep` | Search for patterns in files |
| `egrep` | Extended `grep` (deprecated; use `grep -E`) |
| `fgrep` | Fixed-string `grep` (deprecated; use `grep -F`) |
| `head` | Output the first part of files |
| `iconv` | Convert text from one encoding to another |
| `join` | Join lines of two files on a common field |
| `less` | Pager for viewing text files |
| `more` | Pager for viewing text files |
| `nl` | Number lines of files |
| `pr` | Format text for printing |
| `ptx` | Produce a permuted index of file contents |
| `rev` | Reverse lines character-wise |
| `sed` | Stream editor for filtering and transforming text |
| `sort` | Sort lines of text files |
| `split` | Split a file into pieces |
| `tac` | Concatenate and print files in reverse |
| `tail` | Output the last part of files |
| `tr` | Translate or delete characters |
| `tsort` | Sort and check for duplicates |
| `uniq` | Filter adjacent matching lines |
| `wc` | Count lines, words, and bytes |
| `xargs` | Build and execute commands from standard input |

---

---

## **Process Management**

| Command | Description |
|---------|-------------|
| `at` | Schedule commands to run at a specified time |
| `batch` | Schedule commands to run when system load is low |
| `bg` | Resume a suspended job in the background |
| `crontab` | Tables for driving `cron` (scheduler) |
| `disown` | Remove a job from the shell's job table |
| `fg` | Bring a job to the foreground |
| `jobs` | List active jobs |
| `kill` | Send signals to processes |
| `killall` | Kill processes by name |
| `nice` | Run a command with modified scheduling priority |
| `nohup` | Run a command immune to hangups |
| `pkill` | Signal processes by name |
| `ps` | Report process status |
| `pstree` | Display a tree of processes |
| `renice` | Alter priority of running processes |
| `sleep` | Delay for a specified amount of time |
| `time` | Measure command execution time |
| `top` | Display and update sorted process information |
| `wait` | Wait for background jobs to complete |

---

---

## **System Information**

| Command | Description |
|---------|-------------|
| `arch` | Print machine architecture |
| `cal` | Display a calendar |
| `date` | Print or set the system date and time |
| `dmesg` | Print or control the kernel ring buffer |
| `free` | Display memory usage |
| `hostname` | Show or set the system's host name |
| `id` | Print real and effective user and group IDs |
| `logname` | Print current login name |
| `mpstat` | Report processors related statistics |
| `neofetch` | Display system information (often installed separately) |
| `nproc` | Print the number of processing units available |
| `printenv` | Print all or part of environment |
| `sysctl` | Configure kernel parameters at runtime |
| `tput` | Set terminal-dependent capabilities |
| `uname` | Print system information |
| `uptime` | Tell how long the system has been running |
| `users` | Print the user names of users currently logged in |
| `vmstat` | Report virtual memory statistics |
| `w` | Show who is logged on and what they are doing |
| `who` | Print information about current users |
| `whoami` | Print effective user ID |

---

---
## **Networking**

| Command | Description |
|---------|-------------|
| `curl` | Transfer data from or to a server |
| `dig` | DNS lookup utility |
| `host` | DNS lookup utility |
| `ifconfig` | Configure network interfaces (deprecated; use `ip`) |
| `ip` | Show / manipulate routing, devices, policy routing, and tunnels |
| `netstat` | Print network connections, routing tables, etc. |
| `nslookup` | Query Internet name servers interactively |
| `nmap` | Network exploration tool and security / port scanner |
| `nc` | Netcat: arbitrary TCP and UDP connections and listens |
| `ping` | Send ICMP ECHO_REQUEST to network hosts |
| `route` | Show / manipulate the IP routing table |
| `scp` | Secure copy (remote file copy program) |
| `sftp` | Secure file transfer program |
| `ssh` | OpenSSH remote login client |
| `ssh-keygen` | Generate, manage and convert authentication keys |
| `traceroute` | Print the route packets trace to network host |
| `wget` | Non-interactive network downloader |
| `mtr` | Full round trip time traceroute |

---

---
## **Archiving and Compression**

| Command | Description |
|---------|-------------|
| `7z` | 7-Zip file archiver (high compression) |
| `bunzip2` | Decompress a file (`.bz2`) |
| `bzip2` | Compress a file (`.bz2`) |
| `bzip2recover` | Recover data from damaged `bzip2` files |
| `compress` | Compress data (`.Z`) |
| `cpio` | Copy files to and from archives |
| `gzip` | Compress or expand files (`.gz`) |
| `gunzip` | Decompress a file (`.gz`) |
| `lzcat` | Decompress and concatenate files (`.lz`) |
| `lzma` | Compress or decompress `.xz` and `.lzma` files |
| `lzop` | Compress or decompress files (`.lzo`) |
| `tar` | Archive files |
| `uncompress` | Expand compressed data (`.Z`) |
| `unxz` | Decompress `.xz` files |
| `unzip` | List, test and extract compressed files in a ZIP archive |
| `xz` | Compress or decompress `.xz` files |
| `zip` | Package and compress (archive) files |
| `znew` | Recompress `.Z` files to `.gz` |

---

---
## **User and Group Management**

| Command | Description |
|---------|-------------|
| `addgroup` | Add a user security group |
| `adduser` | Add a user to the system |
| `chage` | Change user password expiry information |
| `chfn` | Change a user's full name, office number, etc. |
| `chpasswd` | Update passwords in batch |
| `chsh` | Change login shell |
| `delgroup` | Remove a group |
| `deluser` | Remove a user from the system |
| `getent` | Get entries from administrative database |
| `groupadd` | Create a new group |
| `groupdel` | Delete a group |
| `groupmod` | Modify a group |
| `groups` | Print the groups a user belongs to |
| `gpasswd` | Administer the `/etc/group` file |
| `id` | Print real and effective user and group IDs |
| `last` | Show a listing of last logged in users |
| `lastlog` | Show when users last logged in |
| `newgrp` | Log in with a new group ID |
| `passwd` | Change user password |
| `su` | Change user ID or become superuser |
| `sudo` | Execute a command as another user |
| `useradd` | Create a new user |
| `userdel` | Delete a user account |
| `usermod` | Modify a user account |

---

---
## **Shell Utilities**

| Command | Description |
|---------|-------------|
| `basename` | Print filename with directory components removed |
| `dirname` | Return directory portion of a pathname |
| `env` | Run a program in a modified environment |
| `expr` | Evaluate expressions |
| `factor` | Factor numbers (print prime factors) |
| `false` | Do nothing, unsuccessfully |
| `hash` | Remember or display command locations |
| `od` | Dump files in octal, hexadecimal, or other formats |
| `pathchk` | Check whether file names are valid or portable |
| `printf` | Format and print data |
| `readlink` | Print value of a symbolic link |
| `realpath` | Print the resolved absolute path name of a file |
| `seq` | Print a sequence of numbers |
| `stat` | Display file or filesystem status |
| `test` | Check file types and compare values |
| `test` / `[` | Evaluate conditional expressions |
| `true` | Do nothing, successfully |
| `tset` | Set terminal modes |
| `tty` | Print the file name of the terminal connected to stdin |
| `uname` | Print system information |
| `yes` | Output a string repeatedly |

---

---
## **Searching and Locating**

| Command | Description |
|---------|-------------|
| `ag` | The Silver Searcher (fast code search) |
| `apropos` | Search the manual page names and descriptions |
| `find` | Search for files in a directory hierarchy |
| `grep` | Search for patterns in files |
| `locate` | Find files by name (uses a pre-built database) |
| `man` | Display manual pages |
| `manpath` | Determine search path for manual pages |
| `pinfo` | View info documents |
| `rg` | Ripgrep: a faster alternative to `grep` |
| `updatedb` | Update the `locate` database |
| `whatis` | Display one-line manual page descriptions |
| `whereis` | Locate the binary, source, and manual page files for a command |

---

---
## **Disk and Filesystem Management**

| Command | Description |
|---------|-------------|
| `badblocks` | Check a device for bad blocks |
| `blkid` | Locate/print block device attributes |
| `blockdev` | Call block device ioctls from the command line |
| `df` | Report filesystem disk space usage |
| `du` | Estimate file space usage |
| `e2fsck` | Check a Linux ext2/ext3/ext4 filesystem |
| `fdisk` | Partition table manipulator |
| `file` | Determine file type |
| `fsck` | Check and repair a Linux filesystem |
| `hdparm` | Get/set hard disk parameters |
| `lsblk` | List block devices |
| `lvm` | Logical Volume Manager |
| `lvcreate` | Create a logical volume |
| `lvdisplay` | Display information about logical volumes |
| `mkfs` | Build a Linux filesystem |
| `mkfs.ext4` | Create an ext4 filesystem |
| `mkswap` | Set up a swap space |
| `mount` | Mount a filesystem |
| `swapon` | Enable devices for paging and swapping |
| `swapoff` | Disable devices for paging and swapping |
| `sync` | Flush filesystem buffers |
| `tune2fs` | Adjust tunable filesystem parameters on ext2/ext3/ext4 |
| `umount` | Unmount file systems |

---
---
## **Job Scheduling**

| Command | Description |
|---------|-------------|
| `anacron` | Run periodic jobs missed by `cron` |
| `at` | Schedule a command to run once at a specified time |
| `atq` | List the user's pending jobs for `at` |
| `atrm` | Remove jobs spooled by `at` |
| `batch` | Schedule commands to run when system load is low |
| `crontab` | Tables for driving `cron` (scheduler) |
| `cron` | Daemon to execute scheduled commands |

---
---
## **Package Management**
*(Commands vary by distribution; listed are the most common)*

| Command | Description | Distribution |
|---------|-------------|--------------|
| `apt` | Package management utility | Debian/Ubuntu |
| `apt-get` | APT package handling utility | Debian/Ubuntu |
| `apt-cache` | Query the APT cache | Debian/Ubuntu |
| `dpkg` | Debian package manager | Debian/Ubuntu |
| `yum` | Package management utility | RHEL/CentOS 7 |
| `dnf` | DNF package manager | Fedora/RHEL 8+ |
| `rpm` | RPM Package Manager | RHEL/Fedora/CentOS |
| `pacman` | Pacman package manager | Arch Linux |
| `zypper` | Command-line package manager | openSUSE |
| `apk` | Alpine Package Keeper | Alpine Linux |
| `emerge` | Portage package manager | Gentoo |
| `npm` | Node.js package manager | Node.js |
| `pip` | Python package installer | Python |
| `gem` | Ruby package manager | Ruby |
| `cargo` | Rust package manager | Rust |
| `brew` | Homebrew package manager | macOS/Linux |
| `conda` | Conda package and environment manager | Anaconda/Miniconda |

---
---
## **Text Editing**

| Command | Description |
|---------|-------------|
| `ed` | Line-oriented text editor |
| `ex` | Line-oriented text editor (extended `ed`) |
| `nano` | Simple terminal-based text editor |
| `sed` | Stream editor for filtering and transforming text |
| `vi` | Visual text editor |
| `vim` | Vi IMproved - enhanced `vi` |
| `emacs` | Extensible, customizable text editor |

---
---
## **System Monitoring and Performance**

| Command | Description |
|---------|-------------|
| `dstat` | Versatile tool for generating system resource statistics |
| `glances` | Comprehensive system monitoring tool |
| `htop` | Interactive process viewer |
| `iostat` | Report Central Processing Unit (CPU) statistics and input/output statistics for devices and partitions |
| `iotop` | Simple top-like I/O monitor |
| `lsof` | List open files |
| `mpstat` | Report processors related statistics |
| `netdata` | Real-time performance monitoring |
| `nmon` | Performance monitoring tool |
| `perf` | Performance counters for Linux |
| `sar` | Collect, report, or save system activity information |
| `strace` | Trace system calls and signals |
| `tload` | Graphic load average display |
| `vmstat` | Report virtual memory statistics |

---
---
## **Security**

| Command | Description |
|---------|-------------|
| `chage` | Change user password expiry information |
| `chmod` | Change file permissions |
| `chown` | Change file ownership |
| `chroot` | Run command or interactive shell with special root directory |
| `gpg` | GNU Privacy Guard (encryption/signing) |
| `gpgv` | Verify OpenPGP signatures |
| `last` | Show a listing of last logged in users |
| `lastlog` | Show when users last logged in |
| `passwd` | Change user password |
| `ssh` | OpenSSH remote login client |
| `ssh-add` | Adds private key identities to the authentication agent |
| `ssh-agent` | Authentication agent |
| `ssh-keygen` | Generate, manage and convert authentication keys |
| `ssh-keyscan` | Gather SSH public keys |
| `sudo` | Execute a command as another user |
| `su` | Change user ID or become superuser |
| `umask` | Set or display the file mode creation mask |
| `w` | Show who is logged on and what they are doing |

---
---
## **Miscellaneous Utilities**

| Command | Description |
|---------|-------------|
| `bc` | An arbitrary precision calculator language |
| `cal` | Display a calendar |
| `clear` | Clear the terminal screen |
| `date` | Print or set the system date and time |
| `dict` | Dictionary client |
| `echo` | Print arguments to stdout |
| `figlet` | Create ASCII art from text |
| `fortune` | Print a random, hopefully interesting, adage |
| `hexdump` | Display file contents in hexadecimal, decimal, octal, or ASCII |
| `iconv` | Convert text from one encoding to another |
| `md5sum` | Compute and check MD5 message digest |
| `mktemp` | Create a temporary file or directory |
| `ncdu` | NCurses Disk Usage |
| `notify-send` | Send desktop notifications |
| `pv` | Monitor the progress of data through a pipe |
| `rename` | Rename multiple files |
| `sha1sum` | Compute and check SHA1 message digest |
| `sha256sum` | Compute and check SHA256 message digest |
| `shuf` | Generate random permutations |
| `sleep` | Delay for a specified amount of time |
| `tee` | Read from standard input and write to standard output and files |
| `timeout` | Run a command with a time limit |
| `tmux` | Terminal multiplexer |
| `tree` | Display directory structure in a tree-like format |
| `watch` | Execute a program periodically, showing output fullscreen |
| `yes` | Output a string repeatedly |