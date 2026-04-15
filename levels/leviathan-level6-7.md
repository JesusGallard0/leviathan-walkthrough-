## Leviathan Level 6-7


### Objective 

Retrieve the password for the next level(no explicit instructions provided)

### Approach
-Listed files and i recognized a setuid file named leviathan6

-Running the binary prompted for a 4-digit PIN

-Attempted dynamic analysis using ltrace and a random 4 digit PIN but no useful function calls or leaks exposed

-Given the constraint(4-digit PIN).The search space is extremely small(10,000 combinations)so it can be brute forced

-Performed a brute-force attack 

-Upon the correct PIN entry,the binary spawned a shell as leviathan7 

-Retrieved the password from the file containing it


### Commands used
   ls

   ./leviathan6

   ltrace ./leviathan6 1234

   for i in {0000..9999}; do ./leviathan6 $i; done
   
   whoami

   cat /etc/leviathan_pass/leviathan7

### Key concepts learned

-Small keyspaces are inherently insecure

-Lack of rate limit enables unrestricted automated attacks
