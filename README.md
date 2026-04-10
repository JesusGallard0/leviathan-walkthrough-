## OverTheWire Leviathan Writeups

#This repository documents my progression through the OverTheWire Leviathan wargame,focusing on linux-based privilege escalation,binary analysis, and common security misconfigurations


### Overwiew
Leviathan is a wargame designed to teach fundamental exploitation techniques in Unix-like environments
It emphasizes practical attack vectors such as insecure file handling,weak authentication mechanisms,and improper binary protections


### Skill demonstrated
-Linux enumeration and filesystem analysis

-identification and exploitation of SUID binaries

-Static and dinamic binary analysis

-Detection of plaintext credential exposure

-Use of command-line tools for information extraction

-Understanding of runtime behavior vs static structure



### Tools & commands used 
    ls, cd ,cat, nano(filesystem navigation and inspection)
    grep(keyword-based data extraction)
    file(file identification)
    strings(static string extraction)
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

### Status

-Levels completed 0-2

-Currently progressing through the wargame
