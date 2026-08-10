# D. Windows CLI Basics

The **Command Prompt (CMD)** is a text-based interface for interacting with the Windows OS.

## Commands

### 1. `cd`

- Shows the full path of the directory you are currently in.
- It is also used to change the current directory.

    cd

### 2. `dir`

- Lists the files and folders present in the current directory.

    dir

### 3. `type`

- Prints the contents of a file in the CMD.

    type <filename>

### 4. Finding a File on the Disk

The `dir` command can be combined with the `/s` flag to search through subdirectories.

    dir /s file.txt

- `/s` tells Windows to search all subfolders starting from the current directory.
- If the file exists, the command displays its full path.

### 5. `whoami`

- Prints the username of the account you are currently logged into.

    whoami

### 6. `hostname`

- Displays the computer's name.

    hostname

### 7. `systeminfo`

- Displays detailed information about the system, including the OS name, OS version, system type, and other system details.

    systeminfo

### 8. `ipconfig`

- Displays the machine's network configuration.
- It can show information such as the IPv4 address, default gateway, and other network details.

    ipconfig
  
