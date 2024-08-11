# Common User & Group Management Commands

## `newgrp`
- **Description:**  
  Temporarily changes the primary group ID (GID) for the current session. This is useful for creating files with a different group ownership without needing to log out and back in.

- **Syntax:**
  ```sh
  newgrp groupname
  ```

- **Example:**
  ```sh
  newgrp developers
  ```
  - Switches the current session's primary group to `developers`.

## `groups`
- **Description:**  
  Displays the groups to which a user belongs.

- **Syntax:**
  ```sh
  groups [username]
  ```

- **Example:**
  ```sh
  groups
  ```
  - Shows the groups of the current user.

  ```sh
  groups alice
  ```
  - Shows the groups that the user `alice` belongs to.

## `gpasswd`
- **Description:**  
  Administers `/etc/group` by allowing you to set or remove passwords for groups, add users to a group, and remove users from a group.

- **Syntax:**
  ```sh
  gpasswd [option] groupname
  ```

- **Common Options:**
  - **`-a username`**: Add a user to a group.
    ```sh
    sudo gpasswd -a alice developers
    ```
    - Adds `alice` to the `developers` group.
  
  - **`-d username`**: Remove a user from a group.
    ```sh
    sudo gpasswd -d alice developers
    ```
    - Removes `alice` from the `developers` group.

  - **`-r`**: Remove the group password.
    ```sh
    sudo gpasswd -r developers
    ```
    - Removes the password from the `developers` group.

## `groupmems`
- **Description:**  
  Manages group memberships by adding or removing members from a group. This command is mainly used on systems that allow group administrators.

- **Syntax:**
  ```sh
  groupmems [option] groupname
  ```

- **Common Options:**
  - **`-a username`**: Add a user to the group.
    ```sh
    sudo groupmems -a alice
    ```
    - Adds `alice` to the group.

  - **`-d username`**: Delete a user from the group.
    ```sh
    sudo groupmems -d alice
    ```
    - Removes `alice` from the group.

  - **`-l`**: List all members of the group.
    ```sh
    sudo groupmems -l
    ```
    - Lists all members of the group.

## `passwd`
- **Description:**  
  Changes a user's password or updates account information.

- **Syntax:**
  ```sh
  passwd [username]
  ```

- **Example:**
  ```sh
  passwd
  ```
  - Changes the password for the current user.

  ```sh
  sudo passwd alice
  ```
  - Changes the password for the user `alice`.

## `su`
- **Description:**  
  Switches to another user account in the current session. When switching to `root`, it is common to use `su` with a hyphen (`-`) to load the root user's environment.

- **Syntax:**
  ```sh
  su [options] [username]
  ```

- **Example:**
  ```sh
  su -
  ```
  - Switches to the root user with the root environment.

  ```sh
  su - alice
  ```
  - Switches to the `alice` user.

## `sudo`
- **Description:**  
  Executes a command as another user, typically the `root` user. It is often used to perform administrative tasks without logging in as `root`.

- **Syntax:**
  ```sh
  sudo [command]
  ```

- **Example:**
  ```sh
  sudo apt update
  ```
  - Runs the `apt update` command with root privileges.

## `usermod`
- **Description:**  
  Modifies user account details, such as username, home directory, shell, and group memberships.

- **Syntax:**
  ```sh
  usermod [options] username
  ```

- **Common Options:**
  - **`-aG groupname`**: Add the user to an additional group.
    ```sh
    sudo usermod -aG developers alice
    ```
    - Adds `alice` to the `developers` group.

  - **`-l new_username`**: Change the username.
    ```sh
    sudo usermod -l newalice alice
    ```
    - Changes the username from `alice` to `newalice`.

  - **`-d /new/home/dir`**: Change the user's home directory.
    ```sh
    sudo usermod -d /new/home/alice alice
    ```
    - Changes `alice`'s home directory to `/new/home/alice`.

## `groupmod`
- **Description:**  
  Modifies a group's properties, such as its name or GID.

- **Syntax:**
  ```sh
  groupmod [options] groupname
  ```

- **Common Options:**
  - **`-n new_groupname`**: Rename a group.
    ```sh
    sudo groupmod -n devs developers
    ```
    - Renames the `developers` group to `devs`.

  - **`-g GID`**: Change the group ID (GID).
    ```sh
    sudo groupmod -g 1001 developers
    ```
    - Changes the `developers` group's GID to `1001`.

---

These commands are essential for managing users and groups on a Linux system, allowing administrators to control access and permissions effectively.