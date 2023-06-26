# Bandit OverTheWire Wargame

Bandit wargame is aimed at absolute beginners. It will teach the basics needed to be able to play other wargames.

It is a 'Capture The Flag' game

----
## To play the game  

You need to connect via ssh. The host to which you need to connect is bandit.labs.overthewire.org, port 2220. username 'bandit0' and password 'bandit0' . 

 ##  " ssh bandit0@bandit.labs.overthewire.org -p 2220  "
----

## Concept
Every level will increase the bandit's username level in the ssh command. Since your username started with 0 (zero) - bandit0@... - once you obtain the password for the next level, simply increase a number in your username

    ssh bandit?-@bandit.labs.overthewire.org -p 2220

---
# Progress

Commands used to find the password and the password itself. 

|Level|Command(s) used|Password|Comments
|--|--|--|--|
|0  |cat readme  |NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL  | - |
|1  |cat < -  |rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi  | - |
|2  |cat spaces\ in\ this\ filename or simply type in "cat spa" and use the tab to autocomplete  |aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG  |-  |
|3  |cat < .hidden  |2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe  |-  |
|4  |`cat -- /home/bandit4/inhere/-*` Password located in "-file07".  |lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR  |-  |
|5  |`find . -size 1033c` `cat < inhere/maybehere07/.file2`  |P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU  |-  |
|6  |`find / -user bandit7 -group bandit6 -size 33c` Locate the only file that doesn't display permission denied.  |z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S  |-  |
|7  |grep "millionth*" data.txt  |TESKZC0XvTetK0S9xNwm25STk5iWrBvP  |- 

# Reference
Reference: https://overthewire.org/wargames/bandit/
