#### `expansion.md`

**Expansion** - Shell expansion enables the use of variables, wildcards, and other features in commands.

- **Types of Expansion:**
  - **Brace Expansion:** `{}` Generate arbitrary strings.
    ```sh
    echo {A..E}  # outputs: A B C D E
    ```
  
  - **Parameter Expansion:** `$` Used to expand variables.
    ```sh
    echo $USER  # outputs the current username
    ```

  - **Command Substitution:** `` ` ` `` or `$()` Executes commands and uses the result.
    ```sh
    echo "Today is $(date)"
    ```

  - **Arithmetic Expansion:** `$(( ))` Perform arithmetic operations.
    ```sh
    echo $((5 + 3))  # outputs: 8
    ```

  - **Tilde Expansion:** `~` Expands to the home directory.
    ```sh
    cd ~  # changes to the home directory
    ```

  - **Pathname Expansion:** `*`, `?` Wildcards for matching filenames.
    ```sh
    ls *.txt  # lists all .txt files
    ```

