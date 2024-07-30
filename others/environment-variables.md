#### `environment-variables.md`

**Environment Variables** - Affect process behavior in Linux.

- **Common Environment Variables:**
  - `$HOME` : User's home directory.
  - `$PATH` : Directories to search for executable files.
  - `$USER` : Current logged-in user.
  - `$SHELL` : Default shell for the user.
  - `$EDITOR` : Default text editor.

- **Setting Environment Variables:**
  ```sh
  export VAR=value  # set 'VAR' to 'value'
  ```

- **Displaying Environment Variables:**
  ```sh
  echo $PATH  # display PATH variable
  ```

- **Using Variables:**
  ```sh
  export GREETING="Hello"
  echo $GREETING  # outputs: Hello
  ```
