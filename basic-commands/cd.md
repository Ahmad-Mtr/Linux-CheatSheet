
# `cd` 

The `cd` (change directory) command is used to navigate between directories in a Linux filesystem.

## Basic Usage

- **Syntax:**

  ```sh
  cd [directory]
  ```

- **Examples:**

  ```sh
  cd /home/user/documents
  ```

  - Changes the current directory to `/home/user/documents`.

  ```sh
  cd ..
  ```

  - Moves up one directory level (to the parent directory).

  ```sh
  cd ~
  ```

  - Changes to the home directory of the current user.

  ```sh
  cd -
  ```

  - Switches to the previous directory you were in.

  ```sh
  cd /
  ```

  - Changes to the root directory.

## Options

The `cd` command itself doesn’t have options, but it works with special characters:

- **`.` (dot):**
  - Refers to the current directory.
  
  ```sh
  cd .
  ```
  
  - No change in directory; stays in the current directory.
  
- **`..` (double dot):**
  - Refers to the parent directory.
  
  ```sh
  cd ..
  ```
  
  - Moves to the parent directory.
  
- **`~` (tilde):**
  - Represents the home directory of the current user.
  
  ```sh
  cd ~
  ```
  
  - Moves to the home directory.
  
- **`-` (dash):**
  - Switches to the previous directory.
  
  ```sh
  cd -
  ```

## Quick Tips

- **No Argument (`cd`):**
  - Running `cd` without any arguments takes you directly to your home directory:
  
  ```sh
  cd
  ```

- **Absolute vs. Relative Path:**
  - You can use absolute paths (starting from `/`) or relative paths (starting from the current directory) with `cd`.

    ```sh
    cd /usr/local/bin   # Absolute path
    cd ../bin           # Relative path
    ```

