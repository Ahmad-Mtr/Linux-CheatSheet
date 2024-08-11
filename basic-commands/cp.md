# `cp` 

The `cp` (copy) command is used to copy files and directories in a Linux filesystem.

## Basic Usage

- **Syntax:**

  ```sh
  cp [options] source destination
  ```

- **Examples:**

  ```sh
  cp file.txt /backup/
  ```

  - Copies `file.txt` to the `/backup/` directory.

  ```sh
  cp file.txt newfile.txt
  ```

  - Copies `file.txt` and names the copy `newfile.txt`.

  ```sh
  cp -r /documents /backup/
  ```

  - Recursively copies the `/documents/` directory and its contents to `/backup/`.

  ```sh
  cp -i file.txt /backup/
  ```

  - Prompts for confirmation before overwriting any existing files in `/backup/`.

  ```sh
  cp -v file.txt /backup/
  ```

  - Verbosely shows what is being copied.

## Common Options

- **`-r` or `--recursive`:**
  - Recursively copies directories and their contents.

  ```sh
  cp -r folder /backup/
  ```

  - Copies the `folder` directory and all its contents to `/backup/`.

- **`-i` or `--interactive`:**
  - Prompts before overwriting files.

  ```sh
  cp -i file.txt /backup/
  ```

  - Asks for confirmation before overwriting `file.txt` in `/backup/`.

- **`-f` or `--force`:**
  - Forces overwriting of existing files without prompting.

  ```sh
  cp -f file.txt /backup/
  ```

  - Overwrites `file.txt` in `/backup/` without confirmation.

- **`-v` or `--verbose`:**
  - Displays what is being copied.

  ```sh
  cp -v file.txt /backup/
  ```

  - Shows that `file.txt` is being copied to `/backup/`.

- **`-u` or `--update`:**
  - Copies only when the source file is newer than the destination file or when the destination file is missing.

  ```sh
  cp -u file.txt /backup/
  ```

  - Updates `file.txt` in `/backup/` only if it is newer than the existing file.

- **`-a` or `--archive`:**
  - Copies files and directories, including attributes like permissions and timestamps, as well as symbolic links.

  ```sh
  cp -a /documents /backup/
  ```

  - Creates an exact copy of `/documents/` in `/backup/`.

- **`--help`:**
  - Displays help information about the `cp` command.

  ```sh
  cp --help
  ```

  - Shows usage information and options.

## Quick Tips

- **Be Mindful of Overwrites:**
  - Without options like `-i`, `cp` will overwrite files in the destination without warning. Use `-i` to prompt before overwriting.

- **Copying Multiple Files:**
  - To copy multiple files to a directory, list the files followed by the destination directory.

  ```sh
  cp file1.txt file2.txt /backup/
  ```

- **Wildcard Usage:**
  - Use wildcards to copy multiple files that match a pattern.

  ```sh
  cp *.txt /backup/
  ```

  - Copies all `.txt` files to the `/backup/` directory.

## Summary

The `cp` command is essential for copying files and directories in Linux. It supports various options to control how files are copied, including recursive copying, prompting before overwrites, and preserving file attributes. Use it carefully, especially when overwriting files.