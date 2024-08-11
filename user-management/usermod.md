# `usermod` 

The `usermod` command is used to modify an existing user account on a Linux system. It allows the system administrator to change a user's account details, such as username, home directory, shell, and group memberships.

## Basic Usage

- **Syntax:**

  ```sh
  usermod [options] username
  ```

- **Examples:**

  ```sh
  sudo usermod -l newusername oldusername
  ```

  - Changes the username from `oldusername` to `newusername`.

  ```sh
  sudo usermod -d /new/home -m username
  ```

  - Changes the user's home directory to `/new/home` and moves the content of the old home directory to the new location.

  ```sh
  sudo usermod -aG sudo username
  ```

  - Adds `username` to the `sudo` group without removing them from other groups.

## Common Options

- **`-l [newname]` or `--login [newname]`:**
  - Changes the username to `newname`.

  ```sh
  sudo usermod -l newusername oldusername
  ```

  - Renames `oldusername` to `newusername`.

- **`-d [dir]` or `--home [dir]`:**
  - Changes the user's home directory to `dir`.

  ```sh
  sudo usermod -d /new/home username
  ```

  - Sets `/new/home` as the home directory for `username`.

- **`-m` or `--move-home`:**
  - Moves the content of the user's current home directory to the new home directory when used with `-d`.

  ```sh
  sudo usermod -d /new/home -m username
  ```

  - Moves the current home directory to `/new/home`.

- **`-s [shell]` or `--shell [shell]`:**
  - Changes the user's login shell to the specified `shell`.

  ```sh
  sudo usermod -s /bin/zsh username
  ```

  - Sets `/bin/zsh` as the default shell for `username`.

- **`-aG [group,...]` or `--append --groups [group,...]`:**
  - Adds the user to the specified supplementary groups without removing them from other groups.

  ```sh
  sudo usermod -aG docker,users username
  ```

  - Adds `username` to the `docker` and `users` groups.

- **`-L` or `--lock`:**
  - Locks the user's password, preventing them from logging in.

  ```sh
  sudo usermod -L username
  ```

  - Locks `username`'s account.

- **`-U` or `--unlock`:**
  - Unlocks the user's password, allowing them to log in again.

  ```sh
  sudo usermod -U username
  ```

  - Unlocks `username`'s account.

- **`-c [comment]` or `--comment [comment]`:**
  - Changes the GECOS (comment) field, often used for the full name of the user.

  ```sh
  sudo usermod -c "John Doe" username
  ```

  - Sets "John Doe" as the comment for `username`.

- **`--help`:**
  - Displays help information about the `usermod` command.

  ```sh
  usermod --help
  ```

  - Shows usage information and available options.

## Quick Tips

- **Renaming a User:**
  - Use `-l` to change a user's login name.

  ```sh
  sudo usermod -l newusername oldusername
  ```

  - Changes the username from `oldusername` to `newusername`.

- **Changing Home Directory:**
  - Use `-d` and `-m` together to move the home directory to a new location.

  ```sh
  sudo usermod -d /new/home -m username
  ```

  - Moves the current home directory to `/new/home`.

- **Managing Group Memberships:**
  - Use `-aG` to add a user to new groups while keeping existing group memberships intact.

  ```sh
  sudo usermod -aG sudo username
  ```

  - Adds `username` to the `sudo` group.

- **Locking/Unlocking Accounts:**
  - Use `-L` to lock and `-U` to unlock user accounts.

  ```sh
  sudo usermod -L username
  ```

  - Locks the `username` account, preventing login.

## Summary

The `usermod` command is a versatile tool for modifying user accounts in Linux. It allows administrators to change various user attributes, such as the username, home directory, shell, and group memberships, as well as lock or unlock accounts. Proper use of `usermod` ensures that user management tasks are performed efficiently and securely.