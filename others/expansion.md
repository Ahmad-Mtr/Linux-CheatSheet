Here's a concise cheatsheet on Expansion and Pattern Matching in Linux, complete with a markdown table of metacharacters and their matches. This can serve as a quick reference for understanding how to use these powerful features in the shell effectively.

---

# Expansion and Pattern Matching Cheatsheet

Linux shells, like Bash, offer various ways to expand variables and match patterns using special characters called metacharacters. These are used in command-line operations, scripting, and file manipulation, making tasks more efficient and versatile.

## Expansion Types

### 1. **Brace Expansion**

Brace expansion is used to generate arbitrary strings by specifying a pattern within braces `{}`.

- **Syntax:**
  
  ```sh
  echo file{1,2,3}.txt
  ```

- **Example:**
  
  ```sh
  touch file{A,B,C}.txt
  # Creates files: fileA.txt, fileB.txt, fileC.txt
  ```

### 2. **Tilde Expansion**

Tilde expansion replaces the tilde `~` with the home directory path of the current user or specified user.

- **Syntax:**
  
  ```sh
  cd ~
  ```

- **Example:**
  
  ```sh
  cd ~/Documents
  # Changes directory to the Documents folder in the home directory
  ```

### 3. **Parameter Expansion**

Parameter expansion is used to manipulate variables and retrieve their values in different ways.

- **Syntax:**
  
  ```sh
  ${parameter}
  ${parameter:-word}  # Use default value if unset
  ```

- **Example:**
  
  ```sh
  NAME="Linux"
  echo ${NAME}          # Outputs: Linux
  echo ${UNSET_VAR:-Default}  # Outputs: Default
  ```

### 4. **Command Substitution**

Command substitution allows the output of a command to replace the command itself in the command line.

- **Syntax:**
  
  ```sh
  $(command)
  `command`
  ```

- **Example:**
  
  ```sh
  TODAY=$(date)
  echo "Today is $TODAY"
  # Outputs: Today is Fri Aug 02 14:21:30 UTC 2024
  ```

### 5. **Arithmetic Expansion**

Arithmetic expansion allows you to perform arithmetic operations using the shell.

- **Syntax:**
  
  ```sh
  $((expression))
  ```

- **Example:**
  
  ```sh
  echo $((5 + 3))
  # Outputs: 8
  ```

### 6. **Pathname Expansion (Globbing)**

Pathname expansion uses wildcards to match filenames and paths.

- **Syntax:**
  
  ```sh
  ls *.txt
  ```

- **Example:**
  
  ```sh
  echo *.txt
  # Matches all files ending with .txt in the current directory
  ```

## Pattern Matching with Metacharacters

Linux shells use metacharacters to match patterns, providing flexibility in file manipulation and command execution. Here is a table of common metacharacters and their functions:

| Metacharacter | Description                                           | Example                  | Matches                             |
|---------------|-------------------------------------------------------|--------------------------|-------------------------------------|
| `*`           | Matches zero or more characters                       | `file*`                  | `file`, `file1`, `file123`, `fileA` |
| `?`           | Matches exactly one character                         | `file?.txt`              | `file1.txt`, `fileA.txt`            |
| `[...]`       | Matches any one of the enclosed characters            | `file[abc].txt`          | `filea.txt`, `fileb.txt`, `filec.txt` |
| `[^...]`      | Matches any one character **not** enclosed            | `file[^abc].txt`         | `filex.txt`, `filey.txt`            |
| `[a-z]`       | Matches any one character in the specified range      | `file[a-c].txt`          | `filea.txt`, `fileb.txt`            |
| `[!a-z]`      | Matches any character **not** in the specified range  | `file[!a-c].txt`         | `filed.txt`, `filex.txt`            |
| `{}`          | Matches any of the patterns separated by commas       | `file{1,2,3}.txt`        | `file1.txt`, `file2.txt`            |
| `{a..z}`      | Matches characters in a specified range (brace expansion) | `file{a..c}.txt` | `filea.txt`, `fileb.txt`, `filec.txt` |
| `\`           | Escapes special characters to treat them literally    | `file\*.txt`             | `file*.txt`                         |

## Pattern Matching Examples

Here's a deeper look into pattern matching using the metacharacters from the table above:

### 1. **Asterisk (`*`)**

- **Example:**
  
  ```sh
  ls *.jpg
  ```

- **Description:**
  - Matches all `.jpg` files, such as `image.jpg`, `photo1.jpg`, and `cat.jpg`.

### 2. **Question Mark (`?`)**

- **Example:**
  
  ```sh
  ls file?.txt
  ```

- **Description:**
  - Matches `file1.txt`, `file2.txt`, etc., but not `file123.txt`.

### 3. **Square Brackets (`[...]`)**

- **Example:**
  
  ```sh
  ls file[123].txt
  ```

- **Description:**
  - Matches `file1.txt`, `file2.txt`, or `file3.txt`.

### 4. **Negated Square Brackets (`[^...]`)**

- **Example:**
  
  ```sh
  ls file[^123].txt
  ```

- **Description:**
  - Matches any file like `filex.txt`, `filea.txt`, but not `file1.txt`, `file2.txt`, or `file3.txt`.

### 5. **Brace Expansion (`{}`)**

- **Example:**
  
  ```sh
  touch {fileA,fileB,fileC}.txt
  ```

- **Description:**
  - Creates `fileA.txt`, `fileB.txt`, `fileC.txt`.

### 6. **Range within Braces (`{a..z}`)**

- **Example:**
  
  ```sh
  echo {a..d}
  ```

- **Description:**
  - Outputs `a b c d`.

## Advanced Pattern Matching Techniques

The shell also provides advanced pattern matching operators like `#`, `%`, `##`, and `%%`, used primarily in parameter expansion:

### 1. **Single Character Match (`#`)**

- **Syntax:**

  ```sh
  ${variable#pattern}
  ```

- **Example:**

  ```sh
  FILENAME="path/to/file.txt"
  echo ${FILENAME#*/}
  # Outputs: "to/file.txt" (removes shortest match from the beginning)
  ```

### 2. **Greedy Character Match (`##`)**

- **Syntax:**

  ```sh
  ${variable##pattern}
  ```

- **Example:**

  ```sh
  FILENAME="path/to/file.txt"
  echo ${FILENAME##*/}
  # Outputs: "file.txt" (removes longest match from the beginning)
  ```

### 3. **Single Character Match from End (`%`)**

- **Syntax:**

  ```sh
  ${variable%pattern}
  ```

- **Example:**

  ```sh
  FILENAME="path/to/file.txt"
  echo ${FILENAME%/*}
  # Outputs: "path/to" (removes shortest match from the end)
  ```

### 4. **Greedy Character Match from End (`%%`)**

- **Syntax:**

  ```sh
  ${variable%%pattern}
  ```

- **Example:**

  ```sh
  FILENAME="path/to/file.txt"
  echo ${FILENAME%%/*}
  # Outputs: "path" (removes longest match from the end)
  ```

### Example: Removing a File Extension

```sh
FILENAME="document.txt"
BASENAME=${FILENAME%.txt}
echo $BASENAME
# Outputs: "document"
```

## Example Commands and Use Cases

Here's a brief walkthrough of some practical examples to demonstrate how expansion and pattern matching can be applied:

### 1. **Renaming Multiple Files**

You can use brace expansion to rename multiple files quickly.

```sh
mv file{1,2}.txt newfile{1,2}.txt
# Renames file1.txt to newfile1.txt and file2.txt to newfile2.txt
```

### 2. **Creating Multiple Directories**

Use brace expansion to create multiple directories with a single command.

```sh
mkdir project/{src,bin,lib,doc}
# Creates directories: project/src, project/bin, project/lib, project/doc
```

### 3. **Finding and Removing Files**

Combining pathname expansion and commands like `find` makes it easy to locate and remove files.

```sh
find . -name "*.log" -type f -delete
# Finds and deletes all .log files in the current directory and subdirectories
```

### 4. **Batch Processing Files**

Using `*` and `?` can help process a batch of files simultaneously.

```sh
cp backup_2024-??.tar.gz /backups
# Copies files like backup_2024-01.tar.gz, backup_202