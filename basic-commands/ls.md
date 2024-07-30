# `ls` Command - Cheat Sheet

The `ls` command is used to list files and directories in Linux. It provides various options to display additional information, sort output, and customize listings.

## Basic Usage

```sh
ls [OPTIONS] [FILE...]
```

- **`OPTIONS`**: Flags to modify the command's behavior.
- **`FILE`**: Specific files or directories to list. Defaults to the current directory if omitted.

## Common Options

| Option     | Description                                                         |
|------------|---------------------------------------------------------------------|
| `-l`       | Long listing format with detailed information.                      |
| `-a`       | Show all files, including hidden files (starting with `.`).         |
| `-h`       | Human-readable sizes (e.g., KB, MB, GB) when used with `-l`.        |
| `-R`       | Recursively list subdirectories.                                    |
| `-t`       | Sort files by modification time, newest first.                      |
| `-S`       | Sort files by size, largest first.                                  |
| `-i`       | Display inode numbers for files and directories.                    |
| `-d`       | List directories themselves, not their contents.                    |
| `-F`       | Append indicator symbols to entries (`/` for directories, etc.).    |
| `-1`       | Display one entry per line.                                         |
| `-r`       | Reverse the order of the sort.                                      |
| `--color`  | Colorize the output based on file type and permissions.             |
| `-A`       | List all files except `.` and `..`.                                 |
| `-v`       | Natural sort of version numbers.                                    |
| `-G`       | Suppress group information in long listing.                         |

### Note:
You can combine options to refine output. For example, `ls -lh` shows a long listing with human-readable file sizes.

## Examples

Here are some practical examples demonstrating how to use the `ls` command:

### Example 1: Basic List

```sh
ls
```

**Description:** Lists files and directories in the current directory.

### Example 2: Detailed List

```sh
ls -l
```

**Description:** Lists files with detailed information such as permissions, owner, size, and modification date.

### Example 3: List Hidden Files

```sh
ls -a
```

**Description:** Lists all files, including hidden files, in the current directory.

### Example 4: Human-Readable Sizes

```sh
ls -lh
```

**Description:** Lists files with sizes displayed in a human-readable format (e.g., KB, MB).

### Example 5: Recursive Listing

```sh
ls -R
```

**Description:** Recursively lists all files and directories, including those in subdirectories.

### Example 6: Sort by Time

```sh
ls -lt
```

**Description:** Lists files sorted by modification time, with the newest files first.

### Example 7: Sort by Size

```sh
ls -lS
```

**Description:** Lists files sorted by size, with the largest files first.

### Example 8: Display Inode Numbers

```sh
ls -i
```

**Description:** Lists files with their inode numbers, useful for identifying files in the filesystem.

### Example 9: Directories Only

```sh
ls -d */
```

**Description:** Lists only directories in the current directory.

### Example 10: Colorized Output

```sh
ls --color=auto
```

**Description:** Displays files with color-coded output for better readability.

### Example 11: Reverse Order

```sh
ls -lr
```

**Description:** Lists files in reverse order, e.g., oldest files first if used with `-t`.

### Example 12: One Entry per Line

```sh
ls -1
```

**Description:** Displays one file per line, useful for piping into other commands.

## Exit Status

- **0**: Success
- **1**: Minor issues (e.g., a file was not found)
- **2**: Serious issues (e.g., command syntax error)

---

This cheat sheet provides a quick reference for the `ls` command, highlighting essential options and practical examples. Use it to efficiently navigate and manage files and directories in your Linux environment.