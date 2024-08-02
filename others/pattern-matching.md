#### `pattern-matching.md`

**Pattern Matching** - File and directory name matching using patterns.

- **Wildcards:**
  - `*` : Matches any number of characters.
    ```sh
    ls *.jpg  # matches all .jpg files
    ```
  
  - `?` : Matches a single character.
    ```sh
    ls file?.txt  # matches file1.txt, file2.txt, etc.
    ```
  
  - `[ ]` : Matches any one of the enclosed characters.
    ```sh
    ls file[12].txt  # matches file1.txt or file2.txt
    ```

- **Example:**
  ```sh
  ls *.log  # list all .log files in the directory
  ```

- **Advanced Patterns:**
  - **Bracket Expressions:** `[a-z]`, `[!abc]`, `[[:digit:]]`
  - **Extended Globbing:** `?(pattern)`, `*(pattern)`, `+(pattern)`, `@(pattern)`, `!(pattern)`
