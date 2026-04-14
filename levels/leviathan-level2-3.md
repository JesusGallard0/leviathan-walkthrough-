## Leviathan Level 2-3


### Objective
Retrieve the password for the next level (no explicit instructions provided)



### Approach
-Listed files in the leviathan2 home directory 

-Recognized a seuid binary"printfile"  

-Observed that its behavior is similar to 'cat' but with some restrictions

-Attempted to read the password file directly but and i got a message (you cant have that file)

-Ran strings on the binary but no useful information

-Used ltrace to analyze runtime behavior
    .Noticed failed access returning -1 indicating improper handling of input

-Suspected that printfile does not properly sanitize user input 

-Considered exploiting shell command injection via filename parsing



-Created a controlled environment in /tmp

-Used touch to create a file with a malicious file name :'hello;vim'
    -hello:valid file name
    -;vim injected command
 
-Executed the binary on my file 

-The binary executed vim due to improper input handling

-Vim ran with leviathan3 privileges due to the setuid


-Inside vim i spawned a shell using :shell

-Now being leviathan 3 i retrieved the password of leviathan3

-Used the password to gain acces in the next level



### Commands used
    -mktemp -d 
    cd /tmp/tmp.gTbnZbzJfK
    touch 'hello;vim'
    $HOME/printfile 'hello;vim'

    #Inside vim
        :shell

    cat /etc/leviathan_pass/leviathan3


    ssh levaithan3@leviathan.labs.overthewire.org -p 2223

### Key concepts learned

-Always consider how user input is parsed,especially in binaries interacting with the shell
-Tools like ltrace are extremely valuable for understanding runtime behavior and spotting weaknesses
