1. use man pages to add a user
```sh
man -k user | grep add

sudo useradd Ahmad
echo "Ahmad:123" | sudo chpasswd
```

2.  
3. location: `/etc/shadow`
```sh
man -k 5 shadow
```
4. Sol:
```sh
tail -n 5 /etc/passwd > ~/password_f
```
### 5. Append the file `password_f` by saving the output of the `whoami` command.

```bash
whoami >> ~/password_f
```


### 6. Redirect the output of the `ls -al` command to the `/tmp/output` file and pass it to the `less` command, so it is displayed on the terminal screen at a time.
```bash
ls -al > /tmp/output less /tmp/output
```

### 7. Find the line that contains the word “root” in the file `/etc/passwd`. Use pipes and grep command.

```bash
cat /etc/passwd | grep "root"
```

### 8. Search for the files whose names contain the word “boot” in your system from your normal user, not as root user, discard error messages. Save the positive results in the file `/tmp/boot-search`.
```bash
find / -name "*boot*" 2>/dev/null > /tmp/boot-search
```
### 9. Print out the value of the variable `~`.

```sh
echo ~
```

### 10. Preview the file `$HISTFILE` using `less`. What’s `$HISTFILE` content?



```bash

`less $HISTFILE`
```
### 11. Use vim to edit the `~/.bashrc` configuration file. Change the value of PS1 variable to be `“PS1="bash\$ "`. Return back to the default PS1 using exactly `[\u@\h \W]\$` as the value of PS1.



```bash
vim ~/.bashrc
```

```bash
PS1="bash\$ "
PS1="[\u@\h \W]\$ "
```
`:wq`

```bash
source ~/.bashrc #Apply the changes
```
### 12. Create a variable called `tmp_path` with the path of the tmp directory, then use it to change to that directory.
```bash
tmp_path="/tmp";
cd $tmp_path;
```
