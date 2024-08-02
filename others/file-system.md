
# Linux Filesystem Directories
here's a diagram showcasing EXT4 directories:
![Linux EXT4 File system Diagram](https://raw.githubusercontent.com/Ahmad-Mtr/Linux-CheatSheet/main/assets/ext4-system.png)


| Directory   | Description                                                                                      | Common Contents                                                         |
| ----------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------- |
| **`/`**     | Root directory, the top-level directory in the filesystem hierarchy.                             | Directories like `bin`, `etc`, `home`, `var`, etc.                      |
| **`/bin`**  | Essential user binaries (executables) needed for basic system operations.                        | Commands like `ls`, `cp`, `mv`, `rm`, `bash`.                           |
| **`/sbin`** | System binaries and executables primarily intended for system administration tasks.              | Commands like `ifconfig`, `fsck`, `reboot`, `shutdown`.                 |
| **`/boot`** | Boot-related files and Kernel itself for starting the system.                                    | Files like `vmlinuz`, `initrd.img`, `grub` directory.                   |
| **`/dev`**  | Device files representing hardware components and virtual devices.                               | Files like `sda`, `tty`, `null`, `random`, `zero`.                      |
| **`/etc`**  | System configuration files and scripts for system-wide settings and services.                    | Files like `passwd`, `hosts`, `fstab`, `init.d`, `systemd` directory.   |
| **`/home`** | User home directories containing personal files and user-specific configuration.                 | Subdirectories like `/home/user1`, `/home/user2`.                       |
| **`/lib`**  | Shared libraries and modules essential for running binaries in `/bin` and `/sbin`.               | Files like `libc.so.6`, `ld-linux.so.2`, kernel modules.                |
| **`/root`** | Home directory for the root user (system administrator).                                         | Personal files and configurations for the root user.                    |
| **`/run`**  | Runtime data, such as system information and temporary files, stored during the system's uptime. | Files like `/run/lock`, `/run/shm`, PID files for services.             |
| **`/sys`**  | Virtual filesystem providing information about devices, drivers, and kernel features.            | Directories like `/sys/class`, `/sys/block`.                            |
| **`/tmp`**  | Temporary files created by applications and the system. Cleared on reboot or periodically.       | Temporary files and directories for short-term use by applications.     |
| **`/usr`**  | Secondary hierarchy for user applications and system utilities, typically read-only.             | Subdirectories like `/usr/bin`, `/usr/lib`, `/usr/share`, `/usr/local`. |
| **`/opt`**  | Optional application software packages and add-on software not part of the default system.       | Application directories, e.g., `/opt/google/chrome`, `/opt/office`.     |
| **`/var`**  | Variable files such as logs, databases, mail, and other frequently changing files.               | Directories like `/var/log`, `/var/spool`, `/var/tmp`, `/var/cache`.    |
| **`/proc`** | Virtual filesystem providing process and system information as files and directories.            | Directories like `/proc/cpuinfo`, `/proc/meminfo`, `/proc/[pid]`.       |

