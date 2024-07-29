## List of Content
- [List of Content](#list-of-content)
- [Get started](#get-started)
- [Basic Commands](#basic-commands)
- [File management Commands](#file-management-commands)
- [User Management](#user-management)
- [Permissions](#permissions)
- [Extra Tips \& Tricks](#extra-tips--tricks)
  - [Alias Command to a one of your own](#alias-command-to-a-one-of-your-own)
- [Contribution](#contribution)
---
## Get started
below are Alternatives to Red Hat's Lab Environment, in which you can use a bash shell to practice all Commands:
- [Github Codespaces](https://github.com/codespaces) (You can also get pro benefits by registering in Github Education [Pack](https://github.com/education/students))
- [Replit](https://replit.com/) ( by creating a simple C project and using the shell there)
-  [Online Linux Terminal](https://cocalc.com/features/terminal)
- Access a local Terminal on Windows via [WSL](https://learn.microsoft.com/en-us/windows/wsl/install)


> [!NOTE]
> You can search 'Fireship Linux' on Youtube for practical & concise 
> Content, see [this](https://youtu.be/LKCVKw9CzFo?feature=shared) for example.

---
## Basic Commands
```sh
# You can use comments like other langs by using the `#`

echo "Hello World" # echo = print


mkdir test  # make directory/folder 'test'
cp src dest  # copy src to dest
rm -rf test # remove recusively & forcefully 'test' and its children

```

```sh
STR="Hello CS416 Students!" # This creates a variable named STR
echo $STR  # Hello ...
```

- **Quotes in Variables**

  - Double quotes `"` allow variable resolution or referencing.

  ```sh
  name="Ahmad"
  greeting="Hello, $name!"
  echo "$greeting" # Hello, Ahmad!
  ```

  - Single quotes `'` do not allow variable resolution.

  ```sh
  name="Ahmad"
  greeting='Hello, $name!' # Notice the double quotes
  echo "$greeting" # Hello, $name!
  ```
## File management Commands
## User Management 

## Permissions

## Extra Tips & Tricks
### Alias Command to a one of your own
- instead of creating files common way; using `touch`, you can alias it to a one of your own:
1. Open `~/.bashrc` (or `~/.bash_profile` if not there) in your editor, using vim for example.
2. add this to the User Aliases section(usually last one)
```sh
Alias batata='touch'
```
3. Source it using `source ~/.bashrc`
4. use `batata file.c` to create Files instead of `touch`

Common aliases include: `ls` to `dir`, `sudo` to `plz`
**Explanation:** Since those Commands are executable binaries, you can can create a Command that aliases/points to an existing Command (which is `touch` in this case)
## Contribution
The Cheatsheet follows a consistent Format, take the `ls` command as an example, You'll find a general use-case & explanation for the Command on this Page, but for extra details,  Options and Others, you'll find a seperate File for this Command if needed.
**Example:**
- README.md
```sh
ls # list Files & Direcctories on this place
```
For extra details visit [ls.md](./basic-commands/ls.md)

- ls.md
Options include: 
	- `-h` for more human readable style.
	-  ...etc.
You can use it to list the Root Directory in a Human-readable format:
```sh
ls -h /
```