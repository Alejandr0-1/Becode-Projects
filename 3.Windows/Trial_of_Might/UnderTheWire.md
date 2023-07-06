# UnderTheWire 
is an awesome website that hosts a number of PowerShell-based wargames meant to help Infosecurity people, either get started with or improve their PowerShell skills.



______

## Century commands used to get them passwords :

______

## Century1 : century1

[no command needed]


___

## Century2 : 

The password for Century2 is the build version of the instance of PowerShell installed on this system.

// To get the build version is as simple as : '$PSVersionTable'

- Answer :  ?


___

## Century 3 :

The password for Century3 is the name of the built-in cmdlet that performs the wget like function within PowerShell PLUS the name of the file on the desktop.

// To find the command behind an alias I used the 'Get-Alias wget' command and got : wget -> Invoke-WebRequest

//  To get the name of the file on the desktop I did 'ls ..\Desktop' and got : 443

- Answer : ?


___

## Century 4 :

The password for Century4 is the number of files on the desktop.

// To get the numbers of files on the desktop I did the (ls -File | Measure-Object).Count

- Answer : ?


___

## Century 5 :

The password for Century5 is the name of the file within a directory on the desktop that has spaces in its name.

// To get the file with spaces I ran the following command : '  ls | Where { $_.Name -Match " " } | % { dir $_ | Select Name }  '

- Answer : ? 



___

## Century 6

The password for Century6 is the short name of the domain in which this system resides in PLUS the name of the file on the desktop.

// To get the short domain I did this command : ' (gwmi Win32_NTDomain).DomainName '

// Which gave me the 'underthewire' value, and if I input ls my output is 3347 which can be used to do ' ls #3347 ' to see the exact file.

- Answer : ?



___


## Century 7

The password for Century7 is the number of folders on the desktop.


// To get that value we can do : ' (ls -Directory | measure).Count '


- Answer : ?


___


## Century 8

The password for Century8 is in a readme file somewhere within the contacts, desktop, documents, downloads, favorites, music, or videos folder in the user’s profile.


// To find the file in the directories I used : ' ls -Recurse '

// Which showed me the .\downloads\ directory where the -'Readme.txt'- file is stored 

// I used the ' cat ' command to output the password 

- Answer : ?

___

## Century 9

The password for Century9 is the number of unique entries within the file on the desktop.

// To get this value I did : ' (cat ..\Desktop\Unique.txt | sort | Get-Unique).count '   

(file parsing)


- Answer : ?

__
 












