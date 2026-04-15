## Leviathan Level 5-6


### Objective
Retrieve the password for the next level(no explicit instructions provided)

### Approach
-Listing files revealed a Setuid binary named leviathan5

-Attempted dynamic analysis using ltrace

-The binary works like this:
    
    -The binary attempts to open and read /tmp/file.log

    -The file does not exists by default

    -The binary trusts this path
    
-Used a symbolic link from the password file to the /tmp/file.log file to open the target file with elevated privileges

-Retrieved the password 

-Used the password to authenticate as leviathan6 in the next level

### Commands used
    ls
    ltrace /leviathan5

    ln -s /etc/leviathan_pass/leviathan6 /tmp/file.log


    ssh leviathan6@leviathan.labs.overthewire.org -p 2223


### Key concepts learned

-Simbolic link attacks redirect file access to sensitive targets

-Avoid using predictable paths in /tmp-Use secure file creation

-Privileges should be dropped before handling user-controlled input
