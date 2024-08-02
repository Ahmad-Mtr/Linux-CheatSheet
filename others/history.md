# `history` Command - Command History in Linux

The `history` command in Linux is a powerful tool for managing and reviewing the command line history. It allows you to view previously executed commands, recall and execute past commands, and even manipulate the command history list.

## Basic Usage

The `history` command displays a list of the most recent commands entered in the terminal session. It’s a handy way to keep track of what you've done and quickly repeat or modify commands.

```sh
history
```

### Example Output

```plaintext
1  ls -al
2  cd /var/www
3  nano index.html
4  git status
5  history
```

In this list, each command is prefixed by a number, which can be used to reference and recall that command.

## Command Options

The `history` command offers several options to manage and utilize the command history:

- **`history n`**: Display the last `n` commands.

  ```sh
  history 10   # Display the last 10 commands
  ```

- **`history -c`**: Clear the command history in the current session.

  ```sh
  history -c   # Clear all commands from history
  ```

- **`history -d offset`**: Delete the command at the specified `offset` position.

  ```sh
  history -d 3  # Delete the command at position 3
  ```

- **`history -a`**: Append the current session's history to the history file (`~/.bash_history`).

  ```sh
  history -a   # Save current session's history to history file
  ```

- **`history -w`**: Write the current session's history to the history file, overwriting it.

  ```sh
  history -w   # Overwrite history file with current session's history
  ```

- **`history -r`**: Read the history file into the current session's history list.

  ```sh
  history -r   # Load history file into current session
  ```

## Recalling and Executing Previous Commands

The `history` command allows you to easily recall and execute previous commands using various shortcuts and substitutions.

### Using Command Numbers

- **Execute a Specific Command**: Use the `!` followed by the command number.

  ```sh
  !3   # Execute the command at position 3 (e.g., 'nano index.html')
  ```

- **Repeat the Last Command**: Use `!!` to repeat the most recent command.

  ```sh
  !!
  ```

- **Execute a Command Starting with a Specific String**: Use `!` followed by the initial characters of the command.

  ```sh
  !gi   # Executes the most recent command that starts with 'gi' (e.g., 'git status')
  ```

### Substitution and Modifications

- **Replace Text in Previous Command**: Use `^old^new` to replace the first occurrence of `old` with `new` in the last command.

  ```sh
  ^nano^vim   # If the last command was 'nano index.html', this changes it to 'vim index.html'
  ```

- **Repeat a Command with a Modification**: Combine history shortcuts with text manipulation.

  ```sh
  !3:s/index.html/about.html/   # Modify the command at position 3 by replacing 'index.html' with 'about.html'
  ```

## Using the `!*` Syntax

The `!*` syntax is a powerful feature of the `history` command that allows you to reuse all the arguments from a previous command in a new command. This is especially useful when you need to perform similar operations on the same set of files or parameters without retyping them.

### Example 1: Reuse Arguments

Suppose you previously executed a command to list files:

```sh
ls -l /home/user/Documents
```

Now you want to change permissions on those same files:

```sh
chmod 755 !*
```

The `!*` syntax expands to `/home/user/Documents`, so the executed command becomes:

```sh
chmod 755 /home/user/Documents
```

### Example 2: Use in Combination with `!n`

You can combine `!*` with other history features to achieve more specific tasks:

```sh
echo "Some text" > /var/log/messages
```

You can repeat the previous command's arguments with another command like `cat`:

```sh
cat !*
```

This command expands to:

```sh
cat /var/log/messages
```

### Example 3: Modifying a Previous Command

Let's say you ran the following command:

```sh
cp file1.txt file2.txt /backup/directory/
```

You can use `!*` to repeat the arguments but with a different command:

```sh
mv !*
```

This results in:

```sh
mv file1.txt file2.txt /backup/directory/
```

This way, you can efficiently reuse the arguments from a previous command, saving time and reducing errors.

## Configuring History Behavior

The behavior of the `history` command can be customized through various shell environment variables.

### Environment Variables

- **`HISTSIZE`**: Controls the number of commands to keep in the history list.

  ```sh
  export HISTSIZE=1000   # Set the history list size to 1000 commands
  ```

- **`HISTFILESIZE`**: Determines the maximum number of lines to store in the history file.

  ```sh
  export HISTFILESIZE=2000  # Set the history file size to 2000 lines
  ```

- **`HISTCONTROL`**: Controls how duplicate commands are treated in history.

  ```sh
  export HISTCONTROL=ignoredups  # Ignore duplicate commands in history
  ```

- **`HISTIGNORE`**: Specifies patterns of commands to exclude from history.

  ```sh
  export HISTIGNORE="ls:cd:pwd:exit"  # Exclude these commands from history
  ```

### Configuring History for Your Shell

You can add these settings to your shell configuration file (e.g., `.bashrc`, `.zshrc`) to persist them across sessions.

```sh
# Example .bashrc configuration
HISTSIZE=1000
HISTFILESIZE=2000
HISTCONTROL=ignoredups
HISTIGNORE="ls:cd:pwd:exit"
```

## Conclusion

The `history` command is a versatile tool for managing your command line experience in Linux. By understanding how to leverage its features, you can enhance your efficiency and productivity when working in the terminal.

For further information, consult the `man` page by running:

```sh
man history
```

---

This `history.md` file provides a comprehensive guide to using the `history` command in Linux, including the `!*` syntax, which allows you to easily recall arguments from previous commands. If you need further assistance with other commands or topics, feel free to ask!