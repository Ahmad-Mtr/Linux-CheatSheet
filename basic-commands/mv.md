# `mv`

The `mv` (move) command is used to move or rename files and directories in a Linux filesystem.

## Basic Usage

- **Syntax:**

  ```sh
  mv [options] source destination
  ```

- **Examples:**

  ```sh
  mv file.txt /backup/
  ```

  - Moves `file.txt` to the `/backup/` directory.

  ```sh
  mv file.txt newfile.txt
  ```

  - Renames `file.txt` to `newfile.txt`.

  ```sh
  mv /documents /backup/
  ```

  - Moves the `/documents/` directory to `/backup/`.

  ```sh
  mv -i file.txt /backup/
  ```

  - Prompts for confirmation before overwriting any existing files in `/backup/`.

  ```sh
  mv -v file.txt /backup/
  ```

  - Verbosely shows what is being moved.

## Common Options

- **`-i` or `--interactive`:**
  - Prompts before overwriting files.

  ```sh
  mv -i file.txt /backup/
  ```

  - Asks for confirmation before overwriting `file.txt` in `/backup/`.

- **`-f` or `--force`:**
  - Forces overwriting of existing files without prompting.

  ```sh
  mv -f file.txt /backup/
  ```

  - Overwrites `file.txt` in `/backup/` without confirmation.

- **`-v` or `--verbose`:**
  - Displays what is being moved or renamed.

  ```sh
  mv -v file.txt /backup/
  ```

  - Shows that `file.txt` is being moved to `/backup/`.

- **`-u` or `--update`:**
  - Moves only when the source file is newer than the destination file or when the destination file is missing.

  ```sh
  mv -u file.txt /backup/
  ```

  - Updates `file.txt` in `/backup/` only if it is newer than the existing file.

- **`--help`:**
  - Displays help information about the `mv` command.

  ```sh
  mv --help
  ```

  - Shows usage information and options.

## Quick Tips

- **Renaming Files or Directories:**
  - The `mv` command can be used to rename files or directories by specifying a new name as the destination.

  ```sh
  mv oldname.txt newname.txt
  ```

- **Moving Multiple Files:**
  - To move multiple files to a directory, list the files followed by the destination directory.

  ```sh
  mv file1.txt file2.txt /backup/
  ```

- **Wildcard Usage:**
  - Use wildcards to move multiple files that match a pattern.

  ```sh
  mv *.txt /backup/
  ```

  - Moves all `.txt` files to the `/backup/` directory.

- **No Undo:**
  - The `mv` command does not create copies; it moves the file or directory. Be cautious, as there is no undo.

## Summary

The `mv` command is essential for moving and renaming files and directories in Linux. It provides options to control overwriting, prompting, and verbosity. Use it carefully, especially when moving important files, as there is no undo for a move operation.