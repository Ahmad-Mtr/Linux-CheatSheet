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
