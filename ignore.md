Below is a list of common Linux commands with brief descriptions and examples. For more detailed explanations and options, please follow the links to the specific `.md` files.

### Table of Contents

- [Basic Commands](#basic-commands)
- [System Information](#system-information)
- [File Compression and Archiving](#file-compression-and-archiving)
- [Text Processing](#text-processing)
- [Advanced Commands and Topics](#advanced-commands-and-topics)
- [User Management Commands](#user-management-commands)

---

## Basic Commands

1. **`ls`** - List files and directories.
   ```sh
   ls  # list files and directories in the current location
   ```
   For extra details, visit [ls.md](./basic-commands/ls.md).

2. **`cd`** - Change directory.
   ```sh
   cd /path/to/directory  # change to the specified directory
   ```
   For extra details, visit [cd.md](./basic-commands/cd.md).

3. **`pwd`** - Print working directory.
   ```sh
   pwd  # display the current directory path
   ```

4. **`mkdir`** - Create a new directory.
   ```sh
   mkdir new_directory  # create a new directory named 'new_directory'
   ```

5. **`rmdir`** - Remove an empty directory.
   ```sh
   rmdir old_directory  # remove the empty directory 'old_directory'
   ```

6. **`touch`** - Create an empty file or update the timestamp of an existing file.
   ```sh
   touch newfile.txt  # create a new empty file named 'newfile.txt'
   ```

7. **`rm`** - Remove files or directories.
   ```sh
   rm file.txt  # remove the file named 'file.txt'
   ```
   For extra details, visit [rm.md](./basic-commands/rm.md).

8. **`cp`** - Copy files or directories.
   ```sh
   cp source.txt destination.txt  # copy 'source.txt' to 'destination.txt'
   ```
   For extra details, visit [cp.md](./basic-commands/cp.md).

9. **`mv`** - Move or rename files and directories.
   ```sh
   mv oldname.txt newname.txt  # rename 'oldname.txt' to 'newname.txt'
   ```
   For extra details, visit [mv.md](./basic-commands/mv.md).

10. **`cat`** - Concatenate and display file contents.
    ```sh
    cat file.txt  # display the contents of 'file.txt'
    ```

11. **`echo`** - Display a line of text.
    ```sh
    echo "Hello, World!"  # print 'Hello, World!' to the terminal
    ```

12. **`head`** - Output the first part of files.
    ```sh
    head file.txt  # display the first 10 lines of 'file.txt'
    ```
    For extra details, visit [head.md](./basic-commands/head.md).

13. **`tail`** - Output the last part of files.
    ```sh
    tail file.txt  # display the last 10 lines of 'file.txt'
    ```
    For extra details, visit [tail.md](./basic-commands/tail.md).

14. **`less`** - View file contents interactively.
    ```sh
    less file.txt  # view 'file.txt' in interactive mode
    ```

15. **`more`** - View file contents one page at a time.
    ```sh
    more file.txt  # view 'file.txt' one page at a time
    ```

16. **`find`** - Search for files in a directory hierarchy.
    ```sh
    find /path -name "filename"  # find 'filename' within '/path'
    ```
    For extra details, visit [find.md](./basic-commands/find.md).

17. **`grep`** - Search text using patterns.
    ```sh
    grep "pattern" file.txt  # search for 'pattern' in 'file.txt'
    ```
    For extra details, visit [grep.md](./text-processing/grep.md).

18. **`chmod`** - Change file permissions.
    ```sh
    chmod 755 script.sh  # set execute permissions for 'script.sh'
    ```
    For extra details, visit [chmod.md](./basic-commands/chmod.md).

19. **`chown`** - Change file owner and group.
    ```sh
    chown user:group file.txt  # change owner and group of 'file.txt'
    ```
    For extra details, visit [chown.md](./basic-commands/chown.md).

20. **`man`** - Display the manual page for a command.
    ```sh
    man ls  # show the manual page for the 'ls' command
    ```
    For extra details, visit [man.md](./advanced/man.md).

21. **`wc`** - Print newline, word, and byte counts for each file.
    ```sh
    wc file.txt  # display line, word, and byte count of 'file.txt'
    ```
    For extra details, visit [wc.md](./basic-commands/wc.md).

22. **`date`** - Display or set the system date and time.
    ```sh
    date  # display the current system date and time
    ```
    For extra details, visit [date.md](./basic-commands/date.md).

23. **`file`** - Determine file type.
    ```sh
    file file.txt  # determine the type of 'file.txt'
    ```
    For extra details, visit [file.md](./basic-commands/file.md).

24. **`history`** - Display or manipulate the command history.
    ```sh
    history  # show the command history
    ```
    For extra details, visit [history.md](./advanced/history.md).

25. **`ln`** - Create links between files.
    ```sh
    ln source.txt link.txt  # create a hard link named 'link.txt' to 'source.txt'
    ```
    For extra details, visit [ln.md](./basic-commands/ln.md).

---

## System Information

26. **`uname`** - Print system information.
    ```sh
    uname -a  # display all system information
    ```
    For extra details, visit [uname.md](./system-info/uname.md).

27. **`df`** - Display disk space usage.
    ```sh
    df -h  # display disk space in human-readable format
    ```

28. **`du`** - Estimate file and directory space usage.
    ```sh
    du -sh /path  # show total size of '/path'
    ```
    For extra details, visit [du.md](./system-info/du.md).

29. **`top`** - Display real-time system processes.
    ```sh
    top  # show running processes and system statistics
    ```
    For extra details, visit [top.md](./system-info/top.md).

30. **`htop`** - Interactive process viewer.
    ```sh
    htop  # interactive system monitor with more features than 'top'
    ```

31. **`ps`** - Report a snapshot of current processes.
    ```sh
    ps aux  # list all running processes with detailed information
    ```
    For extra details, visit [ps.md](./system-info/ps.md).

32. **`kill`** - Terminate processes.
    ```sh
    kill PID  # terminate the process with specified PID
    ```
    For extra details, visit [kill.md](./system-info/kill.md).

33. **`uptime`** - Show how long the system has been running.
    ```sh
    uptime  # display system uptime and load average
    ```

34. **`free`** - Display memory usage.
    ```sh
    free -h  # show memory usage in human-readable format
    ```

35. **`who`** - Show who is logged into the system.
    ```sh
    who  # list users currently logged in
    ```

36. **`hostname`** - Show or set the system's hostname.
    ```sh
    hostname  # display current hostname
    ```

37. **`dmesg`** - Print kernel ring buffer messages.
    ```sh
    dmesg | less  # view kernel messages interactively
    ```

38. **`lscpu`** - Display CPU architecture information.
    ```sh
    lscpu  # show CPU architecture details
    ```

39. **`lsblk`** - List block devices.
    ```sh
    lsblk  # display information about block devices
    ```

40. **`ifconfig`** - Configure network interfaces (deprecated, use `ip`).
    ```sh
    ifconfig  # display network interface information
    ```
    For extra details, visit [ifconfig.md](./system-info/ifconfig.md).

41. **`ip`** - Show/manipulate routing, devices, policy routing.
    ```sh
    ip addr show  # display IP addresses for all interfaces
    ```
    For extra details, visit [ip.md](./system-info/ip

.md).

42. **`ping`** - Send ICMP ECHO_REQUEST to network hosts.
    ```sh
    ping example.com  # ping 'example.com' to check connectivity
    ```

43. **`netstat`** - Print network connections, routing tables, etc.
    ```sh
    netstat -tuln  # list listening ports and connections
    ```

44. **`ss`** - Another utility to investigate sockets.
    ```sh
    ss -tuln  # display open ports and connections
    ```

45. **`traceroute`** - Trace the route to a network host.
    ```sh
    traceroute example.com  # show the path packets take to 'example.com'
    ```

---

## File Compression and Archiving

46. **`tar`** - Archive files.
    ```sh
    tar -cvf archive.tar /path  # create 'archive.tar' from '/path'
    ```
    For extra details, visit [tar.md](./file-compression/tar.md).

47. **`gzip`** - Compress files.
    ```sh
    gzip file.txt  # compress 'file.txt' to 'file.txt.gz'
    ```

48. **`gunzip`** - Decompress files.
    ```sh
    gunzip file.txt.gz  # decompress 'file.txt.gz'
    ```

49. **`zip`** - Package and compress files.
    ```sh
    zip archive.zip file1 file2  # compress 'file1' and 'file2' into 'archive.zip'
    ```

50. **`unzip`** - Extract compressed files.
    ```sh
    unzip archive.zip  # extract 'archive.zip'
    ```

---

## Text Processing

51. **`awk`** - Pattern scanning and processing language.
    ```sh
    awk '{print $1}' file.txt  # print the first column of 'file.txt'
    ```

52. **`sed`** - Stream editor for filtering and transforming text.
    ```sh
    sed 's/old/new/g' file.txt  # replace 'old' with 'new' in 'file.txt'
    ```
    For extra details, visit [sed.md](./text-processing/sed.md).

53. **`cut`** - Remove sections from each line of files.
    ```sh
    cut -d ',' -f 1 file.csv  # extract the first column from 'file.csv'
    ```

54. **`sort`** - Sort lines of text files.
    ```sh
    sort file.txt  # sort lines in 'file.txt'
    ```

55. **`uniq`** - Report or omit repeated lines.
    ```sh
    uniq sorted.txt  # remove duplicate lines in 'sorted.txt'
    ```

---

## Advanced Commands and Topics

56. **`ln`** - Create links between files.
    ```sh
    ln source.txt link.txt  # create a hard link named 'link.txt' to 'source.txt'
    ```
    For extra details, visit [ln.md](./basic-commands/ln.md).

57. **Expansion** - Shell expansion allows you to use variables, wildcards, and other features in commands.
    ```sh
    echo {1..5}  # generates a sequence: 1 2 3 4 5
    ```
    For extra details, visit [expansion.md](./advanced/expansion.md).

58. **Pattern Matching** - Matching file and directory names using patterns.
    ```sh
    ls *.txt  # list all '.txt' files in the directory
    ```
    For extra details, visit [pattern-matching.md](./advanced/pattern-matching.md).

59. **Redirect & Pipelines** - Redirect input and output, and use pipelines to connect commands.
    ```sh
    ls > files.txt  # redirect output of 'ls' to 'files.txt'
    ```
    ```sh
    cat file.txt | grep "pattern"  # use a pipeline to search 'pattern' in 'file.txt'
    ```
    For extra details, visit [redirect-pipelines.md](./advanced/redirect-pipelines.md).

60. **Environment Variables** - Variables that affect the way processes run on your system.
    ```sh
    echo $PATH  # display the current PATH environment variable
    ```
    For extra details, visit [environment-variables.md](./advanced/environment-variables.md).

---

## User Management Commands

61. **`useradd`** - Create a new user account.
    ```sh
    useradd newuser  # create a user named 'newuser'
    ```
    For extra details, visit [useradd.md](./user-management/useradd.md).

62. **`usermod`** - Modify a user account.
    ```sh
    usermod -aG groupname username  # add 'username' to 'groupname'
    ```
    For extra details, visit [usermod.md](./user-management/usermod.md).

63. **`userdel`** - Delete a user account.
    ```sh
    userdel username  # delete the user 'username'
    ```
    For extra details, visit [userdel.md](./user-management/userdel.md).

64. **`passwd`** - Change a user password.
    ```sh
    passwd username  # change password for 'username'
    ```
    For extra details, visit [passwd.md](./user-management/passwd.md).

65. **`groupadd`** - Create a new group.
    ```sh
    groupadd groupname  # create a group named 'groupname'
    ```
    For extra details, visit [groupadd.md](./user-management/groupadd.md).

66. **`groupdel`** - Delete a group.
    ```sh
    groupdel groupname  # delete the group named 'groupname'
    ```
    For extra details, visit [groupdel.md](./user-management/groupdel.md).

67. **`groups`** - Show group memberships.
    ```sh
    groups username  # display groups 'username' belongs to
    ```

---

### Detailed Command Files

For commands that require additional explanations, options, or examples, create markdown files as follows:

#### `grep.md`

**`grep`** - Search text using patterns.

- **Options:**
  - `-i` : Ignore case distinctions.
  - `-r` : Read all files under each directory, recursively.
  - `-v` : Invert match to select non-matching lines.
  - `-n` : Prefix each line of output with the line number within its input file.
  - `-l` : Print file names with matches, once for each file.
  - `-c` : Suppress normal output, counting lines matching instead.

- **Example:**
  ```sh
  grep -i "error" /var/log/syslog  # search for 'error' in '/var/log/syslog', ignoring case
  ```

- **Common Use Cases:**
  - **Search for a string in a file:**
    ```sh
    grep "hello" file.txt
    ```

  - **Search recursively in directories:**
    ```sh
    grep -r "pattern" /path/to/dir
    ```

  - **Count matching lines:**
    ```sh
    grep -c "pattern" file.txt
    ```

#### `expansion.md`

**Expansion** - Shell expansion enables the use of variables, wildcards, and other features in commands.

- **Types of Expansion:**
  - **Brace Expansion:** `{}` Generate arbitrary strings.
    ```sh
    echo {A..E}  # outputs: A B C D E
    ```
  
  - **Parameter Expansion:** `$` Used to expand variables.
    ```sh
    echo $USER  # outputs the current username
    ```

  - **Command Substitution:** `` ` ` `` or `$()` Executes commands and uses the result.
    ```sh
    echo "Today is $(date)"
    ```

  - **Arithmetic Expansion:** `$(( ))` Perform arithmetic operations.
    ```sh
    echo $((5 + 3))  # outputs: 8
    ```

  - **Tilde Expansion:** `~` Expands to the home directory.
    ```sh
    cd ~  # changes to the home directory
    ```

  - **Pathname Expansion:** `*`, `?` Wildcards for matching filenames.
    ```sh
    ls *.txt  # lists all .txt files
    ```

#### `pattern-matching.md`

**Pattern Matching** - File and directory name matching using patterns.

- **Wildcards:**
  - `*` : Matches any number of characters.
    ```sh
    ls *.jpg  # matches all .jpg files
    ```
  
  - `?` : Matches a single character.
    ```sh
    ls file?.txt  # matches file1.txt, file2.txt, etc.
    ```
  
  - `[ ]` : Matches any one of the enclosed characters.
    ```sh
    ls file[12].txt  # matches file1.txt or file2.txt
    ```

- **Example:**
  ```sh
  ls *.log  # list all .log files in the directory
  ```

- **Advanced Patterns:**
  - **Bracket Expressions:** `[a-z]`, `[!abc]`, `[[:digit:]]`
  - **Extended Globbing:** `?(pattern)`, `*(pattern)`, `+(pattern)`, `@(pattern)`, `!(pattern)`

#### `redirect-pipelines.md`

**Redirect & Pipelines** - Managing

 input/output in Linux commands.

- **Redirection Operators:**
  - `>` : Redirect standard output.
    ```sh
    echo "Hello" > file.txt  # write 'Hello' to 'file.txt'
    ```
  
  - `>>` : Append standard output.
    ```sh
    echo "World" >> file.txt  # append 'World' to 'file.txt'
    ```
  
  - `<` : Redirect standard input.
    ```sh
    sort < file.txt  # sort lines from 'file.txt'
    ```
  
  - `2>` : Redirect standard error.
    ```sh
    ls /nonexistent 2> error.log  # redirect errors to 'error.log'
    ```

- **Pipelines (`|`):**
  - Connect multiple commands.
    ```sh
    cat file.txt | grep "pattern" | sort  # chain commands with pipes
    ```

- **Examples:**
  ```sh
  ls -l > filelist.txt  # save the output to 'filelist.txt'
  ```

  ```sh
  grep "error" syslog | less  # view matching lines with 'less'
  ```

#### `environment-variables.md`

**Environment Variables** - Affect process behavior in Linux.

- **Common Environment Variables:**
  - `$HOME` : User's home directory.
  - `$PATH` : Directories to search for executable files.
  - `$USER` : Current logged-in user.
  - `$SHELL` : Default shell for the user.
  - `$EDITOR` : Default text editor.

- **Setting Environment Variables:**
  ```sh
  export VAR=value  # set 'VAR' to 'value'
  ```

- **Displaying Environment Variables:**
  ```sh
  echo $PATH  # display PATH variable
  ```

- **Using Variables:**
  ```sh
  export GREETING="Hello"
  echo $GREETING  # outputs: Hello
  ```

#### `useradd.md`

**`useradd`** - Create new user accounts.

- **Options:**
  - `-m` : Create the user's home directory.
  - `-G` : Add user to additional groups.
  - `-s` : Specify user's login shell.
  - `-c` : Add a comment about the user.

- **Example:**
  ```sh
  useradd -m -s /bin/bash -G sudo newuser  # create a user with a home directory and add to 'sudo' group
  ```

- **Common Use Cases:**
  - **Create a User:**
    ```sh
    useradd -m username
    ```

  - **Add a User to a Group:**
    ```sh
    useradd -G groupname username
    ```

### Directory Structure

Here is the updated directory structure for the cheat sheet project, including the new sections:

```plaintext
.
├── README.md
├── basic-commands
│   ├── cd.md
│   ├── cp.md
│   ├── find.md
│   ├── grep.md
│   ├── head.md
│   ├── ls.md
│   ├── mv.md
│   ├── rm.md
│   ├── chmod.md
│   ├── chown.md
│   ├── tail.md
│   ├── wc.md
│   ├── date.md
│   ├── file.md
│   ├── ln.md
│   └── ...
├── file-compression
│   ├── tar.md
│   └── ...
├── system-info
│   ├── du.md
│   ├── ifconfig.md
│   ├── ip.md
│   ├── kill.md
│   ├── ps.md
│   ├── top.md
│   ├── uname.md
│   └── ...
├── text-processing
│   ├── grep.md
│   ├── sed.md
│   └── ...
├── advanced
│   ├── man.md
│   ├── history.md
│   ├── expansion.md
│   ├── pattern-matching.md
│   ├── redirect-pipelines.md
│   ├── environment-variables.md
│   └── ...
└── user-management
    ├── useradd.md
    ├── usermod.md
    ├── userdel.md
    ├── passwd.md
    ├── groupadd.md
    ├── groupdel.md
    └── ...
```

This structure provides a comprehensive guide to Linux commands and topics, categorized for easy navigation and deeper learning. Each markdown file should include detailed explanations, options, examples, and common use cases to help users master Linux commands effectively.