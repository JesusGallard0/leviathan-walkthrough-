## Leviathan level 1-2


### Objective
Retrieve the password for the next level(no explicit instructions provided)


### Approach
-Listed files in the directory and identified a setuid binary named check
-Executed the bianry and observed that it prompts for a password
-Used file to inspect the binary 
-Attempted static inspection with strings,but no useful information was revealed
-Switched to dynamic analysis using ltrace to monitor library calls during execution
-Observed a string comparision function where the input password was being compared against the correct password
-Ltrace exposed the actual password in plaintext during the comparision
-Used the password to authenticate as leviathan2


### Commands used
    ls -a
    ./check
    file ./check
    srings ./check
    ltrace ./check
        #placed any password and it compared it with the real password

    #Retrieved the password
    

    ssh leviathan2@leviathan.labs.overthewire.org -p 2223


### Key concepts learned

-Dynamic analysis with ltrace allows inspection of library calls ,revealing runtime behavior
