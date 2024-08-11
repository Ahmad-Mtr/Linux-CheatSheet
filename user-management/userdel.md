# `userdel`

The `userdel` command is used to delete a user account and related files from a Linux system. This command allows the system administrator to remove users and their associated directories.

## Basic Usage

- **Syntax:**

  ```sh
  userdel [options] username
  ```

- **Examples:**

  ```sh
  sudo userdel username
  ```

  - Deletes the user account `username` but does not remove the user's home directory.

  ```sh
  sudo userdel -r username
  ```

  - Deletes the user account `username` and removes their home directory and mail spool.

## Common Options

- **`-r` or `--remove`:**
  - Removes the user's home directory and mail spool along with the user account.

  ```sh
  sudo userdel -r username
  ```

  - Deletes `username`'s account, home directory, and mail spool.

- **`-f` or `--force`:**
  - Forces the removal of the user account, even if the user is currently logged in. This option may also remove the user from certain files like `/etc/passwd` and `/etc/shadow`.

  ```sh
  sudo userdel -f username
  ```

  - Forcibly deletes the `username` account, even if the user is logged in.

- **`-Z` or `--selinux-user`:**
  - Removes any SELinux user mapping for the user to be deleted.

  ```sh
  sudo userdel -Z username
  ```

  - Deletes `username` and removes any associated SELinux user mapping.

- **`--help`:**
  - Displays help information about the `userdel` command.

  ```sh
  userdel --help
  ```

  - Shows usage information and available options.

## Quick Tips

- **Deleting a User Safely:**
  - The basic `userdel` command removes the user but leaves their home directory and files intact. Use `-r` to remove the home directory if you want a clean deletion.

  ```sh
  sudo userdel -r username
  ```

  - Deletes the user and their home directory.

- **Forcing Deletion:**
  - Use `-f` if you need to delete a user who is currently logged in or if you encounter issues with a standard deletion.

  ```sh
  sudo userdel -f username
  ```

  - Forcefully deletes the user account, even if they are logged in.

- **Post-Deletion Cleanup:**
  - After deleting a user, you may want to check and manually clean up any remaining files or processes related to that user.

  ```sh
  ps -u username
  ```

  - Lists any processes still running under the deleted user's account.

## Summary

The `userdel` command is essential for managing user accounts on a Linux system. It provides a straightforward way to remove users, with options to delete their home directories, mail spools, and force removal if necessary. Proper usage of `userdel` ensures that user accounts are securely and thoroughly removed when no longer needed.