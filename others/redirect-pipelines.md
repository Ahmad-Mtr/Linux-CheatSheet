#### `redirect-pipelines.md`

**Redirect & Pipelines** - Managing

 input/output in Linux commands.

- **Redirection Operators:**
  - `>` : Redirect standard output.
    ```sh
    echo "Hello" > file.txt  # write 'Hello' to 'file.txt'
    ```
  
  - `>>` : Append standard output.
    ```sh
    echo "World" >> file.txt  # append 'World' to 'file.txt'
    ```
  
  - `<` : Redirect standard input.
    ```sh
    sort < file.txt  # sort lines from 'file.txt'
    ```
  
  - `2>` : Redirect standard error.
    ```sh
    ls /nonexistent 2> error.log  # redirect errors to 'error.log'
    ```

- **Pipelines (`|`):**
  - Connect multiple commands.
    ```sh
    cat file.txt | grep "pattern" | sort  # chain commands with pipes
    ```

- **Examples:**
  ```sh
  ls -l > filelist.txt  # save the output to 'filelist.txt'
  ```

  ```sh
  grep "error" syslog | less  # view matching lines with 'less'
  ```

