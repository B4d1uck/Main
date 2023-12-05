# SCREEN SESSION

## What is a Screen Session?
```bash
screen -S main
```

1. `screen`: `screen` is terminal multiplexer that allows you to run multiple terminal sessions within a single terminal window. It's particularly useful when you want to keep processes running even after you disconnect from a remote server or terminal. It's commonly used for managing and organizing multiple processes or tasks in a Unix-like environment.
2. `-S main`: The `-S` option followed by a session name (in this case, "main") is used to create a new `screen` session and assign it a specific name. This is beneficial when you have multiple `screen` sessions, as it makes it easier to identify and reconnect to the desired session later.

### When you execute the command `screen -S main`:

1. If a `screen` session with the name "main" already exists, you will be reattached to that session.
2. If no `screen` session with the name "main" exists, a new session named "main" will be created.

Once inside the `screen` session, you can run commands and start processes. To detach from the `screen` session and leave it running in the background, you can press `Ctrl + A` followed by `Ctrl + D`. Later, you can reattach to this session using the `screen -r` command.

This command is especially useful for running long-term processes or tasks that you want to keep running even when your terminal connection is closed. The session name ("main" in this case) helps you identify and manage your `screen` sessions effectively.

## Screen -ls
```bash
screen -ls
```

1. `-ls`: The `-ls` option is used to list all the `screen` sessions that are currently running or detached. It provides information about the available `screen` sessions, including their session names and statuses.

### When you execute the command `screen -ls`:

1. The terminal will display a list of `screen` sessions, including their session names, status (whether attached or detached), and other details.
   Example output:
   ```bash
   There is a screen on:
           12345.main    (Detached)
   1 socket in /run/screen/S-your_username.
   ```
   In this example, there is a `screen` session named "main" with the session ID (12345) and the status "Detached".
2. If there are no `screen` sessions, the output will indicate that there are no sockets found.

This command is helpful for checking the status and names of existing `screen` sessions. It allows users to identify active sessions, their statuses, and choose which session to reattach to or manipulate further.

## Starting a Screen Session

Using the mehodology of "check, change, check" we can start a `screen` session by:
```bash
screen -ls
```
This checks if any `screen` sessions are open. Now we can change or open a new `screen` session with:
```bash
screen -S main
```
Lastly, check the `screen` session to make sure it is working properly:
```bash
screen -ls
```


## Keyboard Shortcuts
Keyboard shortcuts within a `screen` session:
1. `Ctrl + a`:
   1. Purpose: Command prefix.
   2. Usage: Prefix for most other `screen` commands
2. `Ctrl + a + c`:
   1. Purpose: Create a new shell session (window).
   2. Usage: Opens a new shell session within the current `screen` window.
3. `Ctrl + a + n`:
   1. Purpose: Switch to the next window.
   2. Usage: Move to the next shell session (window) within the `screen` session.
4. `Ctrl + a + p`:
   1. Purpose:Switch to the previous window.
   2. Usage: Move to the previous shell session (window) within the `screen` session.
5. `Ctrl + a + "`:
   1. Purpose: List and navigate through open windows.
   2. Usage: Presents a list of open windows for selection.
6. `Ctrl + a + A`:
   1. Purpose: Rename the current window.
   2. Usage: Allows you to assign a specific name to the current shell session (window).
7. `Ctrl + a + d`:
   1. Purpose: Detach from the current `screen` session.
   2. Usage: Leaves the `screen` session running in the background.
8. `Ctrl + a + [ or Space`:
   1. Purpose: Enter copy mode.
   2. Usage: Allows you to scroll and copy text within the `screen` session.
9. `Ctrl + a + ]`:
   1. Purpose: Paste copied text.
   2. Usage: Pastes the text copied in copy mode.
10. `Ctrl + a + \`:
    1. Purpose: Kill the current window.
    2. Usage: Closes the current shell session (window).
11. `Ctrl + a + S`:
    1. Purpose: Split the current region horizontally.
    2. Usage: Divides the window into two horizontal regions.
12. `Ctrl + a + Tab`:
    1. Purpose: Switch focus to the next region.
    2. Usage: Moves the focus between split regions

These are just a few of the many `screen` keyboard shortcuts. The flexibility of `screen` allows users to manage multiple sessions, windows, and panes efficiently. For more details, you can refer to the `screen` manual (`man screen`) or online resources.
   
