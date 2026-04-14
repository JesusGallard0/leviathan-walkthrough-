## OverTheWire Leviathan Writeups

#This repository documents my progression through the OverTheWire Leviathan wargame, focusing on linux-based privilege escalation, binary analysis, and common security misconfigurations


### Overwiew
Leviathan is a wargame focused on practical exploitation in unix-like environments
It introduces core offensive security concepts such as:

-Privilege escalation via misconfigures SUID binaries

-Information disclosure through insecure implementations

-Weak input handling and command injection

-Improper storage and handling of sensitive data

### Skill demonstrated
-Linux enumeration and filesystem analysis

-identification and exploitation of SUID binaries

-Static and dinamic binary analysis('strings', 'ltrace')

-Detection of insecure credential handling (plaintext exposure)

-Command injection and input validation bypass techniques

-Understanding of runtime behavior vs static binary structure



### Tools & commands used 
    ls, cd ,cat, nano(filesystem navigation and inspection)
    grep(keyword-based data extraction)
    file(file type identification)
    strings(static string extraction )
    ltrace(dynamic tracing of library calls)
    ssh(remote authentication)

### Repository structure

-Each level is documented in its own file 

-Every writeup includes: 

-Objective---what the level requires 

-Approach---step-by-step methodology 

-Commands used---exact commands executed 

-Key concepts learned---technical takeaway



### Learning Focus

Understanding how real-world vulnerabilities emerge from simple mistakes

Developing a methodology:
    enumeration-analysis-hypothesis-exploitation

Building intuition for where sensitive data is likely to be exposed



### Relevance to Cybersecurity
The techniques practiced in Leviathan directly map to real-world scenarios:

-Misconfigured permissions-privilege escalation

-Hardcoded or exposed credentials-unauthorized access

-Insecure binary design-information disclosure

-Improper input handling-Command injection

### Status

-Levels completed 0-5

-Currently progressing through the wargame
