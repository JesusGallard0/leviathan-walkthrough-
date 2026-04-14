## Leviathan Level 4-5


### Objective 
Retrieve the password for the next level(no explicit instructions provided)


### Approach
-Listed files, including hidden ones using ls -a 

-Discovered a hidden directory named .trash

-Navigated into the directory and found a binary file named bin

-Executed the file and the output consisted of a sequence of binary digits 

-Converted the binary sequence into human readable text using an online tool

-The decoded output revealed the password for leviathan5

### Commands used
    ls -a
    cd .trash
    ./bin

    #Decoded binary output to ASCII 

    -ssh leviathan5@leviathan.labs.overthewire.org -p 2223


### Key concepts learned


-Encoding data is not encryption

-Easily reversible with minimal effort

-Binary sequences can represent ASCII characters directly


