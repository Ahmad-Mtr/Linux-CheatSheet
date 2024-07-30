#### `grep.md`

**`grep`** - Search text using patterns.

- **Options:**
  - `-i` : Ignore case distinctions.
  - `-r` : Read all files under each directory, recursively.
  - `-v` : Invert match to select non-matching lines.
  - `-n` : Prefix each line of output with the line number within its input file.
  - `-l` : Print file names with matches, once for each file.
  - `-c` : Suppress normal output, counting lines matching instead.

- **Example:**
  ```sh
  grep -i "error" /var/log/syslog  # search for 'error' in '/var/log/syslog', ignoring case
  ```

- **Common Use Cases:**
  - **Search for a string in a file:**
    ```sh
    grep "hello" file.txt
    ```

  - **Search recursively in directories:**
    ```sh
    grep -r "pattern" /path/to/dir
    ```

  - **Count matching lines:**
    ```sh
    grep -c "pattern" file.txt
    ```
