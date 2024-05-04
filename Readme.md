lvl0 :
used ssh bandit0@bandit.labs.overthewire.org -p 2220
and the password id bandit0
lvl0-lvl1:
used cat readme to get password for next lvl
lvl1-lvl2:
used cat "-" to get password for next lvl or we 
can use cat ./- to get the password
lvl2-lvl3:
used cat "spaces in filename"
lvl3-lvl4:
first cd inhere
then used find to get the file
lvl4-lvl5:
first used "file ./inhere" to get file07 has ascii text
then used cat ./inhere/-file07 to get the password
lvl5-lvl6:
cd inhere 
then used find -size to get file of size -1033c then got file07 in which password was stored
lvl6-lvl7:
find  / -type f -user bandit7 -group bandit6 -size 33c
type f for onlhy searching the file ignore the directories
lvl7-lvl8:
used "grep millionth data.txt"
lvl8-lvl9:
sort data.txt then uniq data.txt to get the password
lvl9-lvl10:
just used cat data.txt then there was only one line which has several '='
lvl10-lvl11:
simple base64 -d data.txt
lvl11-lvl12:
used google for this to get the tr command
cat data.txt | "tr 'A-Za-z' 'N-ZA-Mn-za-m'"
lvl12-lvl13:
first made a temp directory using mktmp -d
then inside it used cp ~/data.txt to coopy it in the temp directory
then used xxd -r to revert it into a binary file
then used file command to get to know what type of compression and decompress using diff type of compression and got the password
lvl13-lvl14:
bandit 13 had file named sshkey.private which had the rsa private key which is used to access the another user without knowing the private key tehn used
ssh -i sshkey.private bandit14@localhost
in bandit14 used "cat  /etc/bandit_pass/bandit14" to get the password
lvl14-lvl15:
"openssl s_client --connect localhost:30000"
then copy pasted the password of the last lvl to get the password for next lvl