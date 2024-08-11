Here's a concise explanation for the `passwd` command in Linux, including options, usage, and a short explanation:

---

# `passwd` Command Cheatsheet

The `passwd` command is used to change a user's password in Linux. It can be used by both normal users to change their own password and by the system administrator to manage passwords for other users.

## Basic Usage

- **Syntax:**

  ```sh
  passwd [options] [username]
  ```

- **Examples:**

  ```sh
  passwd
  ```

  - Prompts the current user to change their password.

  ```sh
  sudo passwd username
  ```

  - Changes the password for the specified `username` (requires superuser privileges).

## Common Options

- **`-l` or `--lock`:**
  - Locks the password of the specified user, effectively disabling their account.

  ```sh
  sudo passwd -l username
  ```

  - Locks the account of `username`, preventing them from logging in.

- **`-u` or `--unlock`:**
  - Unlocks the password of the specified user, re-enabling their account.

  ```sh
  sudo passwd -u username
  ```

  - Unlocks the account of `username`, allowing them to log in again.

- **`-d` or `--delete`:**
  - Deletes the password for the specified user, making it impossible to log in using a password.

  ```sh
  sudo passwd -d username
  ```

  - Deletes the password for `username`, allowing login only via other authentication methods.

- **`-e` or `--expire`:**
  - Forces the user to change their password at the next login.

  ```sh
  sudo passwd -e username
  ```

  - Expires the password for `username`, requiring a password change at the next login.

- **`-x [days]` or `--maxdays [days]`:**
  - Sets the maximum number of days a password is valid before it must be changed.

  ```sh
  sudo passwd -x 90 username
  ```

  - Sets the password for `username` to expire after 90 days.

- **`-n [days]` or `--mindays [days]`:**
  - Sets the minimum number of days before a user can change their password again.

  ```sh
  sudo passwd -n 7 username
  ```

  - Prevents `username` from changing their password for 7 days after the last change.

- **`-w [days]` or `--warndays [days]`:**
  - Sets the number of days before password expiration that the user will be warned.

  ```sh
  sudo passwd -w 7 username
  ```

  - Warns `username` 7 days before their password expires.

- **`--help`:**
  - Displays help information about the `passwd` command.

  ```sh
  passwd --help
  ```

  - Shows usage information and available options.

## Quick Tips

- **Changing Your Own Password:**
  - Simply type `passwd` and follow the prompts to change your password.

  ```sh
  passwd
  ```

  - Prompts you to enter your current password and the new password.

- **Forcing a Password Change:**
  - Use `-e` to require a user to change their password at the next login.

  ```sh
  sudo passwd -e username
  ```

  - Forces `username` to change their password upon the next login.

- **Locking and Unlocking Accounts:**
  - Use `-l` to lock and `-u` to unlock user accounts.

  ```sh
  sudo passwd -l username
  ```

  - Locks the `username` account, preventing login.

- **Setting Password Expiration:**
  - Control how often users must change their passwords with `-x` and `-n` options.

  ```sh
  sudo passwd -x 60 -n 1 username
  ```

  - Requires `username` to change their password every 60 days, with at least 1 day between changes.

## Summary

The `passwd` command is essential for managing user passwords on a Linux system. It allows users to change their own passwords and administrators to enforce password policies, such as expiration and account locking. Proper use of `passwd` ensures secure and controlled access to user accounts.