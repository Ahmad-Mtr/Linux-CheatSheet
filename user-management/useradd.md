# `useradd` 

The `useradd` command is used to create a new user account on a Linux system. It allows the system administrator to specify various attributes for the new user, such as home directory, shell, and group memberships.

## Basic Usage

- **Syntax:**

  ```sh
  useradd [options] username
  ```

- **Examples:**

  ```sh
  sudo useradd newuser
  ```

  - Creates a new user account named `newuser` with default settings.

  ```sh
  sudo useradd -m -s /bin/bash newuser
  ```

  - Creates a new user account named `newuser`, with a home directory and Bash as the default shell.

  ```sh
  sudo useradd -G sudo newuser
  ```

  - Creates a new user account named `newuser` and adds them to the `sudo` group.

## Common Options

- **`-m` or `--create-home`:**
  - Creates the user's home directory if it does not exist.

  ```sh
  sudo useradd -m newuser
  ```

  - Creates a home directory `/home/newuser` for the user `newuser`.

- **`-s [shell]` or `--shell [shell]`:**
  - Specifies the user's login shell.

  ```sh
  sudo useradd -s /bin/bash newuser
  ```

  - Sets `/bin/bash` as the default shell for `newuser`.

- **`-G [group,...]` or `--groups [group,...]`:**
  - Adds the user to one or more supplementary groups.

  ```sh
  sudo useradd -G sudo,users newuser
  ```

  - Adds `newuser` to the `sudo` and `users` groups.

- **`-d [dir]` or `--home [dir]`:**
  - Specifies the home directory for the user.

  ```sh
  sudo useradd -d /custom/home newuser
  ```

  - Sets `/custom/home` as the home directory for `newuser`.

- **`-c [comment]` or `--comment [comment]`:**
  - Adds a comment (often the full name of the user) to the account.

  ```sh
  sudo useradd -c "John Doe" newuser
  ```

  - Sets "John Doe" as the GECOS (comment) field for `newuser`.

- **`-e [date]` or `--expiredate [date]`:**
  - Sets the account expiration date.

  ```sh
  sudo useradd -e 2024-12-31 newuser
  ```

  - Expires the account `newuser` on December 31, 2024.

- **`-f [days]` or `--inactive [days]`:**
  - Specifies the number of days after a password expires until the account is disabled.

  ```sh
  sudo useradd -f 30 newuser
  ```

  - Disables `newuser`'s account 30 days after the password expires.

- **`--help`:**
  - Displays help information about the `useradd` command.

  ```sh
  useradd --help
  ```

  - Shows usage information and available options.

## Quick Tips

- **Creating a User with Default Settings:**
  - Simply use `useradd` followed by the username.

  ```sh
  sudo useradd username
  ```

  - Creates the user with default settings, but without a home directory or password.

- **Creating a User with a Home Directory and Shell:**
  - Use the `-m` and `-s` options to create a more fully configured user.

  ```sh
  sudo useradd -m -s /bin/zsh username
  ```

  - Creates a user with a home directory and sets the Zsh shell as default.

- **Adding a User to Groups:**
  - Use the `-G` option to add the user to multiple groups during account creation.

  ```sh
  sudo useradd -G wheel,docker username
  ```

  - Adds the user to the `wheel` and `docker` groups.

- **Setting an Expiration Date:**
  - Use `-e` to specify when the user account should expire.

  ```sh
  sudo useradd -e 2025-01-01 username
  ```

  - Expires the account on January 1, 2025.

## Summary

The `useradd` command is a powerful tool for creating new user accounts on a Linux system. It allows for significant customization during account creation, including setting home directories, shells, group memberships, and more. Understanding the key options of `useradd` can help efficiently manage users in a Linux environment.