# Excalibur
Excalibur is an Eternalblue exploit based "Powershell" for the Bashbunny project.
It's purpose is to reflect on how a "simple" USB drive can execute the 7 cyber kill chain.
Excalibur may be used only for demostrations purposes only, and the developers are not responsible to any misuse or illeagal usage.


# What does it do?
When Excalibur gets connected to the machine, it will run the following:

1. Trys to bypass UAC, or just get administrative rights
2. Gets interface info (IP addresses) and build a network map inside a TXT file.
3. Scans port 445 for the known "MS10-17" ("EternalBlue") vulnerability in every segment found.
4. Exploits every machine and drop a shell to a remote machine.


# How to?
Follow the steps here to compile a shellcode:
https://github.com/vivami/MS17-010

1. Copy payload.txt to the switch folder.
2. Copy the "eternablblue_exploit7.py" and compile it using Pyinstaller:
* "pip install pyinstaller"
* "pipinstaller --onefile eternablblue_exploit7.py"

3. Add your shellcode and the compiled exploiter into "a.zip" and copy it to the "loot" folder".
* a.zip needs to contain a compiled, standalone eternalblue exploiter from "vivami's" repo and the shellcode.

4. Copy the powershell script to (p_v2.ps1) to the loot folder.


# TODO
1. Add persistency in terms of add a new user account, and persistent shell.
2. Exploit other machines and applications in the network, with the credentials added in the persistency step.
3. Exfiltrate sensitive data from the network, outside.
4. Bug fixes, and exploits stabilizations.


# Notes
Excalibur is still in Beta, bugs are iminent.
