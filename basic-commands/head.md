
# `head` Command - Cheat Sheet

The `head` command in Linux is used to display the first few lines of a file or standard input. By default, it prints the first 10 lines, but this can be adjusted using various options.

## Basic Usage

```sh
head [OPTIONS] [FILE...]
```

- **`OPTIONS`**: Flags to modify the command's behavior.
- **`FILE`**: The file(s) to read from. If omitted, `head` reads from standard input.

## Common Options

| Option     | Description                                                                  |
|------------|------------------------------------------------------------------------------|
| `-n N`     | Display the first **N** lines of each file.                                  |
| `-c N`     | Display the first **N** bytes of each file.                                  |
| `-q`       | Suppress headers when multiple files are being read.                         |
| `-v`       | Always print headers with file names, even if there's only one file.         |
| `-z`       | Use a zero byte (`\0`) as the line delimiter instead of a newline character. |

### Note:
The `head` command can handle multiple files, printing the first lines of each file in succession, with headers unless suppressed with `-q`.

## Examples

Here are some practical examples demonstrating how to use the `head` command:

### Example 1: Display First 10 Lines

```sh
head file.txt
```

**Description:** Displays the first 10 lines of `file.txt`.

### Example 2: Display First 20 Lines

```sh
head -n 20 file.txt
```

**Description:** Displays the first 20 lines of `file.txt`.

### Example 3: Display First 5 Bytes

```sh
head -c 5 file.txt
```

**Description:** Displays the first 5 bytes of `file.txt`. Useful for binary files or examining file headers.

### Example 4: Suppress Headers for Multiple Files

```sh
head -q file1.txt file2.txt
```

**Description:** Displays the first 10 lines of both `file1.txt` and `file2.txt` without headers, outputting them consecutively.

### Example 5: Force Headers for Single File

```sh
head -v file.txt
```

**Description:** Displays the first 10 lines of `file.txt` with a header, useful when the output is piped or redirected.

### Example 6: Read from Standard Input

```sh
echo -e "Line1\nLine2\nLine3" | head -n 2
```

**Description:** Uses a pipe to send text to `head`, which then outputs the first 2 lines.

### Example 7: Display Lines with a Zero Byte Delimiter

```sh
printf "Line1\0Line2\0Line3\0" | head -z -n 2
```

**Description:** Uses the zero byte (`\0`) as the delimiter instead of newlines, displaying `Line1` and `Line2`.

### Example 8: Combining Options

```sh
head -n 15 -v file1.txt file2.txt
```

**Description:** Displays the first 15 lines of `file1.txt` and `file2.txt`, each with a header showing the file name.

### Example 9: Display Lines from Multiple Files

```sh
head -n 3 file1.txt file2.txt
```

**Description:** Displays the first 3 lines from both `file1.txt` and `file2.txt`, each with a header indicating the file name.

### Example 10: Use in Scripts

In scripting, `head` is often used to preview or limit output, such as processing a log file:

```sh
logfile="/var/log/syslog"
head -n 5 $logfile | while read line; do
  echo "Log entry: $line"
done
```

**Description:** Reads the first 5 lines of `/var/log/syslog` and processes each line in a loop.

## Exit Status

- **0**: Success
- **1**: An error occurred (e.g., file not found).

---
