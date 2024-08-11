# `chmod`

The `chmod` (change mode) command is used to change the file permissions for users, groups, and others in a Linux filesystem.

## Basic Usage

- **Syntax:**

  ```sh
  chmod [options] mode file...
  ```

- **Examples:**

  ```sh
  chmod 755 script.sh
  ```

  - Sets the permissions of `script.sh` to `rwxr-xr-x` (owner can read, write, and execute; group and others can read and execute).

  ```sh
  chmod +x script.sh
  ```

  - Adds execute permissions to `script.sh` for all users.

  ```sh
  chmod u=rw,go=r file.txt
  ```

  - Sets the permissions of `file.txt` to `rw-r--r--` (owner can read and write; group and others can read).

  ```sh
  chmod -R 644 /var/www/
  ```

  - Recursively sets the permissions of all files in `/var/www/` to `rw-r--r--`.

## Understanding File Permissions

- **Permissions:**
  - **r**: Read (4)
  - **w**: Write (2)
  - **x**: Execute (1)

- **Permission Sets:**
  - **u**: User (owner)
  - **g**: Group
  - **o**: Others
  - **a**: All (user, group, and others)

- **Numerical Mode:**
  - Permissions can be represented numerically with a 3-digit code.
  - **Example: `755`**
    - **7**: `rwx` (owner)
    - **5**: `r-x` (group)
    - **5**: `r-x` (others)

- **Symbolic Mode:**
  - Permissions can also be set using symbolic notation.
  - **Example: `u=rwx,g=rx,o=rx`**
    - Sets read, write, and execute for the owner, and read and execute for group and others.

## Common Options

- **`-R` or `--recursive`:**
  - Recursively changes permissions for directories and their contents.

  ```sh
  chmod -R 755 /mydir
  ```

  - Applies `755` permissions to `/mydir` and all files and subdirectories within it.

- **`--reference=[rfile]`:**
  - Sets the permissions of a file to match those of another file.

  ```sh
  chmod --reference=reference.txt file.txt
  ```

  - Sets the permissions of `file.txt` to match those of `reference.txt`.

- **`--help`:**
  - Displays help information about the `chmod` command.

  ```sh
  chmod --help
  ```

  - Shows usage information and options.

## Quick Tips

- **Changing Only Specific Permissions:**
  - Use `+`, `-`, or `=` to add, remove, or set specific permissions.

  ```sh
  chmod u+x file.sh
  ```

  - Adds execute permission to the owner of `file.sh`.

- **Common Permission Values:**
  - **`644`**: Owner can read/write, others can read (files).
  - **`755`**: Owner can read/write/execute, others can read/execute (directories).
  - **`700`**: Owner can read/write/execute, others have no permissions.
  - **`777`**: All users can read/write/execute (use with caution).

- **View Current Permissions:**
  - Use `ls -l` to view the current permissions of a file or directory.

  ```sh
  ls -l file.txt
  ```

## Summary

The `chmod` command is essential for managing file and directory permissions in Linux. It allows you to specify who can read, write, or execute a file using either numeric or symbolic modes. Understanding and correctly applying file permissions is crucial for maintaining security and proper access control in your system.