## Leviathan level 0-1



### Objective
Retrieve the password for the  next level(no explicit instructions provided)


### Approach
-Enumered the current directory,including hidden files, using ls -a
-Identified a hidden directory called .backup
-Navigated into the directory and discovered a html file
-Inspected the file contents and recognized it as a saved webpage of a school
-Used grep to search for potential sensitive keywords such as "password" 
-Located a plaintext password embedded within the HTML source
-Used the extracted password to authenticate into the next level


### Commands used
    ls -a 
    cd .backup
    ls
    nano bookmarks.html     #(manual inspection)
        

    grep "password" bookmarks.html


    ssh leviathan1@leviathan.labs.overthewire.org -p 2223




### Key concepts learned

-Hidden files enumeration is critical during initial reconnaissance
-Credentials may be left in client-side files
-Never store credentials in plaintext

