## Leviathan Level 3-4



### Objective
Retrieve the password for the next level (no explicit instructions provided)


### Approach
-Listed files in the leviathan3 directory

-Identified a setuid binary called level3

-Analyzed its behavior using ltrace 

-Observed the program prompts for a password 

-It compares user imput against a hardcoded plaintext password using functions like strcmp

-From the ltrace output,the correct password is visible in plaintext during the comparision

-Ran the binary and placed the password

-A shell was given to me as leviathan4

-Retrieved the password for leviathan4 

-Used the password to gain acces in the next level 

### Commands used 
    ls
    file ./level3
    ltrace ./level3


    ./level3
    #placed the password manually

    #got the shell as leviathan4

    cat /etc/leviathan_pass/leviathan4

### Key concepts learned

-Comparing passwords in plain text is a critical vulnerability
    -Proper implementations should use:
        -Hashed passwords
        -Constant-time comparision functions

-Running the exploit inside ltrace can interfere with execution(since ltrace wraps syscalls and may affect stdin handling)
