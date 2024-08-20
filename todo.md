- [x] Add detailed History Section
- [x] Add Permissions Section
- [x] Create File System Diagram (use lucidchart)
- [ ] Date commands
- [ ] `chage`
- [ ]  `ip addr show`
- [ ] `ping`
- [ ] `ping6`
- [ ] ping -c
- [ ] `ip -br addr show`
- [ ] `ip link show`
- [ ] `ip route`
- [ ] `ip -6 route`
- [ ] `tracepath`
- [ ] `traceroute`
- [ ] `ss` command

#### Useful NetworkManager Commands

The following table lists the key `nmcli` commands that are discussed in this section:

| Command                             | Purpose                                                                  |
| :---------------------------------- | :----------------------------------------------------------------------- |
| `nmcli dev status`                  | Show the NetworkManager status of all network interfaces.                |
| `nmcli con show`                    | List all connections.                                                    |
| ``nmcli con show _`name`_``         | List the current settings for the connection name.                       |
| ``nmcli con add con-name _`name`_`` | Add and name a new connection profile.                                   |
| ``nmcli con mod _`name`_``          | Modify the connection name.                                              |
| `nmcli con reload`                  | Reload the configuration files, after manual file editing.               |
| ``nmcli con up _`name`_``           | Activate the connection name.                                            |
| ``nmcli dev dis _`dev`_``           | Disconnect the interface, which also deactivates the current connection. |
| ``nmcli con del _`name`_``          | Delete the specified connection and its configuration file.              |
