# Proceed after 'grep -C'

# //////////////////////////// A

# ////// alias

# Defines a convenient shorthand for a longer command, to save typing.

> kali@kali:~/Desktop\$ alias

# Output :

alias c='clear'
alias ls='ls --color=auto'
alias t='./t.sh'

# //////////////////////////// B

# ////// bg \*

# Sends a suspended job to run in the background.

# //////////////////////////// C

# ////// cal

# By default, displays a calendar of the current month (current day is highlighted)

> JLs-MacBook-Air:Terminal jl\$ cal

# Output :

     April 2020

Su Mo Tu We Th Fr Sa  
 1 2 3 4  
 5 6 7 8 9 10 11  
12 13 14 15 16 17 18  
19 20 21 22 23 24 25  
26 27 28 29 30

# Turns off highlighting of today (.. of the present day)

> JLs-MacBook-Air:Terminal jl\$ cal -h

# Display Julian days (days one-based, numbered from January 1)

> JLs-MacBook-Air:Terminal jl\$ cal -j

# Output :

        April 2020

Su Mo Tu We Th Fr Sa  
 92 93 94 95  
 96 97 98 99 100 101 102  
103 104 105 106 107 108 109  
110 111 112 113 114 115 116  
117 118 119 120 121

# Display the specified month. For example display April from 2019

> JLs-MacBook-Air:Terminal jl\$ cal -m 3 2019

# Output :

     March 2019

Su Mo Tu We Th Fr Sa  
 1 2  
 3 4 5 6 7 8 9  
10 11 12 13 14 15 16  
17 18 19 20 21 22 23  
24 25 26 27 28 29 30  
31

# Print the country codes

> JLs-MacBook-Air:Terminal jl\$ ncal -p

# Output :

AL Albania 1912-11-30 IT Italy 1582-10-04
AT Austria 1583-10-05 JP Japan 1918-12-18
AU Australia 1752-09-02 LI Lithuania 1918-02-01
BE Belgium 1582-12-14 LN Latin 9999-05-31
BG Bulgaria 1916-03-18 LU Luxembourg 1582-12-14
CA Canada 1752-09-02 LV Latvia 1918-02-01
CH Switzerland 1655-02-28 NL Netherlands 1582-12-14
CN China 1911-12-18 NO Norway 1700-02-18
CZ Czech Republic 1584-01-06 PL Poland 1582-10-04
DE Germany 1700-02-18 PT Portugal 1582-10-04
DK Denmark 1700-02-18 RO Romania 1919-03-31
ES Spain 1582-10-04 RU Russia 1918-01-31
FI Finland 1753-02-17 SI Slovenia 1919-03-04
FR France 1582-12-09 SE Sweden 1753-02-17
GB United Kingdom 1752-09-02 TR Turkey 1926-12-18
GR Greece 1924-03-09 \*US United States 1752-09-02
HU Hungary 1587-10-21 YU Yugoslavia 1919-03-04
IS Iceland 1700-11-16

# Print the number of the week below each week column

> JLs-MacBook-Air:Terminal jl\$ ncal

# Output :

    April 2020

Mo 6 13 20 27  
Tu 7 14 21 28  
We 1 8 15 22 29  
Th 2 9 16 23 30  
Fr 3 10 17 24  
Sa 4 11 18 25  
Su 5 12 19 26

> JLs-MacBook-Air:Terminal jl\$ ncal -w

# Output :

    April 2020

Mo 6 13 20 27  
Tu 7 14 21 28  
We 1 8 15 22 29  
Th 2 9 16 23 30  
Fr 3 10 17 24  
Sa 4 11 18 25  
Su 5 12 19 26  
 14 15 16 17 18

# Display a calendar for the current year

> JLs-MacBook-Air:Terminal jl\$ cal -y

> JLs-MacBook-Air:Terminal jl\$ ncal -y

# Display the previous, current and next month surrounding today

> JLs-MacBook-Air:Terminal jl\$ cal -3

# Display the previous, current and next month surrounding today

> JLs-MacBook-Air:Terminal jl\$ cal -A 2

# Output :

                            2020
       April                  May                   June

Su Mo Tu We Th Fr Sa Su Mo Tu We Th Fr Sa Su Mo Tu We Th Fr Sa  
 1 2 3 4 1 2 1 2 3 4 5 6  
 5 6 7 8 9 10 11 3 4 5 6 7 8 9 7 8 9 10 11 12 13  
12 13 14 15 16 17 18 10 11 12 13 14 15 16 14 15 16 17 18 19 20  
19 20 21 22 23 24 25 17 18 19 20 21 22 23 21 22 23 24 25 26 27  
26 27 28 29 30 24 25 26 27 28 29 30 28 29 30  
 31

# Display the number of months before the current month

> JLs-MacBook-Air:Terminal jl\$ cal -B 2

# ////// cat

# Prints the file's content to standard output. The command is often used to display short text files.

> JLs-MacBook-Air:tutorial jl\$ cat void.txt

# 'cat' command can also be used to join files together. Suppose we have 2 separate .txt (v01.txt & v02.txt) and we want to chain them together :

> JLs-MacBook-Air:Shell jl\$ cat v\*.txt > /Users/jl/Shell/code/tutorial/void.txt

# Output : I heiße euch Willkommen!

# We can also write our standard input to a separate .txt file (like 'la.txt' in Desktop) :

> JLs-MacBook-Air:tutorial jl\$ cat > /Users/jl/Desktop/la.txt
> Welcome!

# We can change direction of standard input from the keyboard to our file.txt. It means, we write something to our .txt file as an input source and let it display the contents like so:

JLs-MacBook-Air:tutorial jl\$ cat < void.txt
la la la la la la la

# Display non-blank numbered lines, starting at 1

> JLs-MacBook-Air:Terminal jl\$ cat void.txt

# Output :

Mike Jones
John Smith
Kathy Jones
Jane Kennedy
John Doe

> JLs-MacBook-Air:Terminal jl\$ cat -b void.txt

# Output :

     1	Mike Jones
     2	John Smith
     3	Kathy Jones
     4	Jane Kennedy
     5	John Doe

# Number the output lines, starting at 1

> JLs-MacBook-Air:Terminal jl\$ cat void.txt

# Output :

Mike Jones

John Smith
Kathy Jones

Jane Kennedy
John Doe

> JLs-MacBook-Air:Terminal jl\$ cat -n void.txt

# Output :

     1	Mike Jones
     2
     3	John Smith
     4	Kathy Jones
     5
     6	Jane Kennedy
     7	John Doe

# Squeeze each sequence if blank lines into a single blank line

> JLs-MacBook-Air:Terminal jl\$ cat void.txt

# Output :

Mike Jones
John Smith
Kathy Jones
Jane Kennedy

John Doe

> JLs-MacBook-Air:Terminal jl\$ cat -s void.txt

# Output :

Mike Jones
John Smith
Kathy Jones
Jane Kennedy

John Doe

# ////// chmod

# The chmod (change mode) command protects files and directories from unauthorized users on the same system, by setting access permissions. Typical premissions are read, write and execute, and they may be limited to the file owner, the file's group owner, and/or other users. Let's list all files :

> JLs-MacBook-Air:Shell jl\$ ls -l

# Output :

total 16
drwxr-xr-x 5 jl staff 160 Apr 13 15:58 code
drwxr-xr-x 2 jl staff 64 Apr 15 17:46 empty
drwxr-xr-x 22 jl staff 704 Apr 1 18:31 lit
-rw-r--r--@ 1 jl staff 67 Apr 14 23:20 v01.txt
-rw-r--r--@ 1 jl staff 150 Apr 13 16:17 v02.txt

# We are interested in particular folder called 'empty'. : Let's see it :

> JLs-MacBook-Air:Shell jl\$ ls -ld empty

# Output :

drwxr-xr-x 2 jl staff 64 Apr 15 17:46 empty

# At this point you have all rights to access the folder. Everyone else can only read or execute it but not write. We can however change it to 'no access' for everyone :

> JLs-MacBook-Air:Shell jl\$ chmod 700 empty

# Output : (7 = 111 for read : 1, write : 1, execute : 1)

drwx------ 2 jl staff 64 Apr 15 17:46

# If you change the right to only execute (x) the directory like this:

> JLs-MacBook-Air:Shell jl\$ chmod 100 empty

# Output : (... you wont have access to folder 'empty' via Finder but only through Terminal via cd command.)

d--x------ 2 jl staff 64 Apr 15 17:46 empty

# ////// chgrp

# The chgrp (change group) command sets the group ownership of files and directories :

> JLs-MacBook-Air:Shared jl\$ chgrp smith file1 file2 folder1

# ////// chown

# Is used to change the owner and group owner of a file or directory. Superuser privileges are required to use this command. Let's say we have two uses: janet, who has access to superuser privileges, and tony, who does not. User janet wants to copy a file from her home directory to the home directory of tony. Because janet wants tony to be able to edit the file, janet changes the ownership of the copied file form janet to tony.

# Example from the book :

> [janet@linuxbox ~]\$ sudo cp myfile.txt ~tony
> Password:

> [janet@linuxbox ~]\$ sudo ls -l ~tony/myfile.txt

# Output :

-rw-r--r-- 1 root root root 2018-03-20 14:30 /home/tony/myfile.txt

> [janet@linuxbox ~]\$ sudo chown tony: ~tony/myfile.txt

> [janet@linuxbox ~]\$ sudo ls -l ~tony/myfile.txt

# Output :

[janet@linuxbox ~]\$ sudo ls -l ~tony/myfile.txt

# ////// cp

# Makes a copy of a file. Next code line performs a copy of a '4_b.jpg' picture into a 'copy' folder:

> jl@JLs-MacBook-Air Terminal % cp 4_b.jpg copy

# Copy a directory hierarchy recursively, preserving all file attributes and links. If you try to copya picture together with an empty folder without '-a', you will fail. In order to this :

> JLs-MacBook-Air:Terminal jl\$ cp -a copy empty

# Output :

(Files are successfully copied to a new folder called 'empty')

# Force the copy. If a destination file exists, overwrite it unconditionally

> JLs-MacBook-Air:Terminal jl\$ cp -f flow.jpg empty

# Interactive mode. Ask (or prompt) before overwriting destination files.

> JLs-MacBook-Air:Terminal jl\$ cp -i flow.jpg empty

# Output :

overwrite empty/flow.jpg? (y/n [n]) y

(overwrites the file)

# Do not overwrite an existing file

> JLs-MacBook-Air:Terminal jl\$ cp -n flow.jpg empty

# Show what and where the files are copied (verbose). Here the image 'flow.jpg' is being copied to 'empty' folder

> JLs-MacBook-Air:Terminal jl\$ cp -v flow.jpg empty

# Output :

flow.jpg -> empty/flow.jpg

# //////////////////////////// D

# ////// date

# Displays the current time and date

> date

# Output : Tue 31 Mar 2020 18:54:09 CEST

# You can format the output differently by supplying a format string beginning with a plus sign :

> kali@kali:~/shell\$ date "+%D"

# Output : 04/27/20

# You can format the output differently by supplying a format string beginning with a plus sign :

> kali@kali:~/shell\$ date "+%D"

# Output :

04/27/20

> kali@kali:~/shell\$ date "+The time is %l:%M %p on a lovely %A in %B"

# Output :

The time is 6:38 PM on a lovely Monday in April

# ////// df

# Sometimes, you need to see how much disk space is available on an individual device. The 'df' command allows you to easily see what's happening on all the mounted disks.

# The command displays the following:

:' ■ The device location of the device
■ How many 1024-byte blocks of data it can hold
■ How many 1024-byte blocks are used
■ How many 1024-byte blocks are available
■ The amount of used space as a percentage
■ The mount point where the device is mounted
'

# Showing the disk space in human-readable form

> JLs-MacBook-Air:Terminal jl\$ df -H

# Output :

Filesystem Size Used Avail Capacity iused ifree %iused Mounted on
/dev/disk1s5 121G 11G 95G 11% 487327 1181331113 0% /
devfs 190k 190k 0B 100% 644 0 100% /dev
/dev/disk1s1 121G 13G 95G 12% 214033 1181604407 0% /System/Volumes/Data
/dev/disk1s4 121G 1.1G 95G 2% 2 1181818438 0% /private/var/vm
map auto_home 0B 0B 0B 100% 0 0 100% /System/Volumes/Data/home

# Display size in megabytes (-m) & only local filesystems, not networked filesystems (-l)

> JLs-MacBook-Air:Terminal jl\$ df -lm

# Output :

Filesystem 1M-blocks Used Available Capacity iused ifree %iused Mounted on
/dev/disk1s5 115411 10616 90729 11% 487327 1181331113 0% /
/dev/disk1s1 115411 12338 90729 12% 214122 1181604318 0% /System/Volumes/Data
/dev/disk1s4 115411 1025 90729 2% 2 1181818438 0% /private/var/vm

# //////////////////////////// E

# ////// eject

# Allows removable media to be ejected under software control. If the device or a device partition is currently mounted, it is unmounted before ejecting. The eject is processed on exclusive open block device file descriptor if --no-unmount or --force are not specified.

# Let's eject a USB device called STICK

> kali@kali:/\$ sudo eject /media/kali/STICK

# Output : (device gets ejected)

# Don't eject, just show device found

> kali@kali:/\$ sudo eject -n /media/kali/STICK

# Output : eject: device is `/dev/sdb1'

# Display version information and exit (enable verbose output)

> kali@kali:/\$ sudo eject -v /media/kali/STICK

# Output :

[sudo] password for kali:
eject: device name is `/media/kali/STICK' eject: expanded name is `/media/kali/STICK'
eject: `/dev/sdb1' is mounted at `/media/kali/STICK'
eject: unmounting device `/dev/sdb1' from `/media/kali/STICK'
eject: `/dev/sdb1' is a multipartition device eject: using device name `/dev/sdb' for ioctls
eject: trying to eject `/dev/sdb' using CD-ROM eject command
eject: CD-ROM eject command succeeded

# //////////////////////////// F

# ////// fdisk

# Allows us to interact directly with disk-like devices (such as hard disk drives and flash drives) at a very low level. With this tool we can edit, delete, and create partitions on the device.

# ////// file

# Reports the type of a file. The output is an educated guess based on the file content and other factors

> jl@JLs-MacBook-Air Terminal % ls
> 4_b.jpg fsoc.m4a fsoc.mp4 macOS_bash.txt void.txt

> jl@JLs-MacBook-Air Terminal % file void.txt
> void.txt: ASCII text

> jl@JLs-MacBook-Air Terminal % file fsoc.mp4
> fsoc.mp4: ISO Media, MP4 v2 [ISO 14496-14]

# ////// find

# Searches one or more directories (and their subdirectories recursively) for files matching certain criteria. F.e. print filenames beginning with "myfile" :

> kali@kali:~\$ find . -type f -name myfile\* -print

# Output :

./shell/myfile1

# ////// free

# Displays the total amount of free and used physical and swap memory in the system, as well as the buffers and caches used by the kernel. Show beneath all output fields automatically scaled to shortest three digit unit and display the units of print out.

> kali@kali:~\$ free -h

# total used free shared buff/cache available

Mem: 1.9Gi 406Mi 1.2Gi 10Mi 339Mi 1.4Gi  
Swap: 2.0Gi 0B 2.0Gi

# //////////////////////////// G

## //////////// gedit <br><br>

Text editors can be invoked from the command line by typing the name of the editor followed by the name of te file you want to edit. If the file does not already exist, the editor will assume that we want to create a new file. Here is an example using _gedit_:

> `>` gedit _some file_

This command will start the _gedit_ text editor and load the file named _some file_, if it exists. <br><br>

## //////////// grep (global regular expression print)

<br>

Is a powerful program used to find text patterns within files. It's used like this

> `>` grep _pattern_ _filename_

Let's use this stack of words

```
duku

sonne

zenit

alfones

petro

valiant

duku

vintar
```

Now let's sort, exclude and print only those expressions out which contain _on_

> `>` less void.txt | sort | uniq | grep on

## Output: <br>

```
alfones

sonne
```

## grep -A

Prints the matched line together with _N_ lines after that (trailing context).

Let's find for example a match to string _"pet"_ and after that print next 2 lines:

> `>` grep -A 2 "pet" v01.txt

## Output:

```
petro

valiant
```

**Explanation:**

First matched string "petro" gets printed followed by empty line and the subsequent string 'valiant')

## grep -B

Same as `grep -A`. Prints match case together with _N_ lines **before** that.

> `>` grep -B 3 "pet" t.txt

## Output:

```

alfones

petro
```

## grep -C

Prints match case as in previous two examples together with _N_ lines in **both** directions.

> `>` grep -C 2 "pet" t.txt

## Output:

```
alfones

petro

valiant
```

## Output:

# Use of this option forces grep to output lines matching the specified pattern

> JLs-MacBook-Air:Shell jl\$ grep -a "ku" v01.txt

# Output :

duku
duku

# In front of each line of matching output, print the byte offset of the line in the input file. The numbering starts at index 0. Empty line counts for 2.

> JLs-MacBook-Air:Shell jl\$ grep -b "ku" v01.txt

# Output :

0:duku
46:duku

> JLs-MacBook-Air:Shell jl\$ grep -b "sonn" v01.txt

# Output :

6:sonne

# Print only a count of matching lines

> JLs-MacBook-Air:Shell jl\$ grep -c "du" v01.txt

# Output :

2

> JLs-MacBook-Air:Shell jl\$ grep -c "sonn" v01.txt

# Output :

1

# Print only the names of files that contain matching lines, not the lines themselves

> JLs-MacBook-Air:Shell jl\$ grep -l "fast" \*.txt

# Output :

v02.txt

# In front of each line of matching output, print its original line number (code line starts with 1)

> JLs-MacBook-Air:Shell jl\$ grep -n "du" v01.txt

# Output :

1:duku
13:duku

# You can search the docs more globally :

> JLs-MacBook-Air:Shell jl\$ grep -n "alfo" \*.txt

# Output :

v01.txt:7:alfones # (document : v01.txt; line : 7)

# Recursively search all files in a directory and its subdirectories. For example search after string "nach" in 'Shell'-directory and its subdirectories

> JLs-MacBook-Air:Shell jl\$ grep -r "nach" ~/Shell/ \*.txt

# Output :

/Users/jl/Shell//code/v03.txt:Herzlich Willkommen nach Hause !

# Match ONLY complete words (i.e., words that match the entire regular expression)

> JLs-MacBook-Air:Shell jl\$ grep -w "petr" \*.txt

# Output : nothing

> JLs-MacBook-Air:Shell jl\$ grep -w "petro" \*.txt

# Output :

v01.txt:petro

# //////////////////////////// H

# ////// halt

# Terminates all running processes. The whole system is stopped and no longer responds to any input. Obviously, such a command can only be executed by root admin. Let's reboot the system :

> kali@kali:~\$ sudo halt --reboot

# Output : (system will restart)

# ////// head

# Prints the first n lines of a file, by default it's 10 lines. Let's print 1st 5 lines of the 'grep' command :

> JLs-MacBook-Air:tutorial jl\$ head -n 5 void.txt

duku

sonne

zenit

# ////// history

# Allows you to recall previous commands you've run - that is, the shell's history - and re-execute them.

> JLs-MacBook-Air:Desktop jl\$ history

# Output :

1 c
2 clear
3 alias te="./test.sh"
...
...
314 history

# Clear (delete) your history :

> JLs-MacBook-Air:Desktop jl\$ history -c

# Re-run command number N in your history. Example shows re-running 5th command

> JLs-MacBook-Air:Desktop jl\$ !5

# //////////////////////////// I

# ////// id

# Every user has a unique, numeric user ID, and a default group with a unique, numeric group ID. The 'id' command prints these values along with their associated user and group names :

> JLs-MacBook-Air:tutorial jl\$ id

# Output :

uid=501(jl) gid=20(staff) groups=20(staff),12(everyone),61(localaccounts), ....

# Display the full name of the user.

> JLs-MacBook-Air:tutorial jl\$ id -F

# Output : JL

# Display the different group IDs (effective, real and supplementary) as white-space separated numbers, in no particular order.

> JLs-MacBook-Air:tutorial jl\$ id -G

# Output :

20 12 61 79 80 81 98 701 33 100 204 250 395 398 399 400

# Display the process audit user ID and other process audit properties, which requires privilege.

> JLs-MacBook-Air:Shell jl\$ id -A

# Output :

auid=501
mask.success=0xffffffff
mask.failure=0xffffffff
termid.port=0x03000002
asid=100006

# ////// ip

# //////////////////////////// K

# ////// kill

# Sends a signal to a process. This can terminate a process (the default action), interrupt it, suspend it, crash it, and so on. Let's start a process called 'xlogo' and display the PID's via ps-command :

> kali@kali:~$ xlogo
> kali@kali:~$ ps

Output :

    PID TTY          TIME CMD

1246 pts/0 00:00:00 bash
2530 pts/0 00:00:00 xlogo
2531 pts/0 00:00:00 ps

Now let's terminate our process :

> kali@kali:~$ kill 2530
> kali@kali:~$ ps

# Output :

    PID TTY          TIME CMD

1246 pts/0 00:00:00 bash
2535 pts/0 00:00:00 ps

# You may also specify signals with numbers. Following example uses signal value 15 which stands for SIGTERM (Terminate. Default signal sent by the kill command) :

> kali@kali:~\$ kill -s 15 2652

# Output : (killed)

# ////// killall

# Sends a signal to all processes running any of the specified commands. If no signal name is specified, SIGTERM is sent. Let's terminate process 'xlogo' and report afterwards if it was successful or not.

> kali@kali:~\$ killall -v TERM xlogo

Killed xlogo(1508) with signal 15
TERM: no process found
[1]+ Terminated xlogo

# //////////////////////////// L

# ////// less

# Is a command to view text files.

# ////// locate

# performs a rapid database search of pathnames and then outputs every name that matches a given substring. Suppose, for example, we want to find all the programs with names that begin with zip. Because we are looking for programs, we can assume that the name of the directory containing the programs would end with bin/ :

> kali@kali:~\$ locate bin/zip

# Output :

/usr/bin/zip
/usr/bin/zipcloak
/usr/bin/zipdetails
/usr/bin/zipgrep
/usr/bin/zipinfo
/usr/bin/zipnote
/usr/bin/zipsplit
/usr/sbin/zip2john

# ////// ls

# Shows the contents and determines a variety of important file and directory attributes. We can simply enter 'ls' to get a list of files and subdirectories contained in the current working directory

# Force output to be one entry per line :

> JLs-MacBook-Air:~ jl\$ pwd

# Output : /Users/jl

> JLs-MacBook-Air:~ jl\$ ls -1

# Output :

Algorithms
C:C++
Computer Networks
Desktop
Documents
Downloads
JS
Library
Movies
Music
Pictures
Public
Shell
Terminal

# List all files (even those with period at the start) :

> JLs-MacBook-Air:~ jl\$ ls -a // (--all)

. .npm JS
.. .vscode Library
.CFUserTextEncoding .zsh_history Movies
.DS_Store Algorithms Music
.Trash C:C++ Pictures
.bash_history Computer Networks Public
.bash_sessions Desktop Shell
.config Documents Terminal
.lesshst Downloads

# Decorate certain filenames with meanignful symbols, indicating their types. Appends :

# "/" to directories

# "\*" to executables

# "@" to symbol links

# "|" to named pipes

# "=" to sockets

> JLs-MacBook-Air:Shell jl\$ ls -F

# Output :

code/ lit/ v01.txt v02.txt

# In order to get additional info we can simly add -l and directory path we wish to look at :

> JLs-MacBook-Air:Shell jl\$ ls -l ~/Terminal

# Output :

total 10736
drwxr-xr-x 3 jl staff 96 Apr 1 18:18 copy
-rw-r--r--@ 1 jl staff 78778 Apr 2 16:49 f001.m4a
-rw-r--r--@ 1 jl staff 40300 Apr 2 16:50 f002.m4a
-rw-r--r--@ 1 jl staff 156586 Apr 2 16:51 f003.m4a
-rw-r--r--@ 1 jl staff 1098100 Jan 7 18:22 fsoc.m4a
-rw-r--r--@ 1 jl staff 4092278 Jan 7 18:21 fsoc.mp4
-rw-r--r--@ 1 jl staff 10394 Jan 22 19:47 macOS_bash.txt
-rw-------@ 1 jl staff 56 Jan 22 19:14 void.txt

# Specify the size of each file :

> JLs-MacBook-Air:Shell jl\$ ls -lh ~/Terminal

# Output :

total 10736
drwxr-xr-x 3 jl staff 96B Apr 1 18:18 copy
-rw-r--r--@ 1 jl staff 77K Apr 2 16:49 f001.m4a
-rw-r--r--@ 1 jl staff 39K Apr 2 16:50 f002.m4a
-rw-r--r--@ 1 jl staff 153K Apr 2 16:51 f003.m4a
-rw-r--r--@ 1 jl staff 1.0M Jan 7 18:22 fsoc.m4a
-rw-r--r--@ 1 jl staff 3.9M Jan 7 18:21 fsoc.mp4
-rw-r--r--@ 1 jl staff 10K Jan 22 19:47 macOS_bash.txt
-rw-------@ 1 jl staff 56B Jan 22 19:14 void.txt

# The table underneath provides notation about 'Shell' directory :

:'
■ drwxr-xr-x : Access rights to the file. The 1st character indicates the type of file which is a "d" (directory). A dash (-) stands for a regular file.  
■ 3 : Number of hard links for the particular file.  
■ jl : The username of the file owner
■ staff : The name of the group that owns the file
■ 96 : Size fo the fule in bytes
■ Mar 31 17:55: Date and time since last modification of the file
■ code : Name of the file  
'

# You can also sort files by modification time :

> JLs-MacBook-Air:Terminal jl\$ ls -lt

# Output :

total 10904
-rw-r--r--@ 1 jl staff 156586 Apr 2 16:51 f003.m4a
-rw-r--r--@ 1 jl staff 40300 Apr 2 16:50 f002.m4a
-rw-r--r--@ 1 jl staff 78778 Apr 2 16:49 f001.m4a
drwxr-xr-x 3 jl staff 96 Apr 1 18:18 copy
-rw-r--r--@ 1 jl staff 10394 Jan 22 19:47 macOS_bash.txt
-rw-------@ 1 jl staff 56 Jan 22 19:14 void.txt
-rw-r--r--@ 1 jl staff 1098100 Jan 7 18:22 fsoc.m4a
-rw-r--r--@ 1 jl staff 4092278 Jan 7 18:21 fsoc.mp4
-rw-r--r--@ 2 jl staff 82080 Aug 15 2019 flow.jpg

# Print the file size allocation in kilobytes, not blocks

> JLs-MacBook-Air:Terminal jl\$ ls -sk

# Output :

total 5368
0 copy 156 f003.m4a 12 macOS_bash.txt
80 f001.m4a 1076 fsoc.m4a 4 void.txt
40 f002.m4a 4000 fsoc.mp4

# List subdirectories recursively and display file's information in one command. 'copy' is here the only folder containing picture file 'flower.jpg'

> JLs-MacBook-Air:Terminal jl\$ ls -Rlh

# Output :

total 10904
drwxr-xr-x 3 jl staff 96B Apr 1 18:18 copy
-rw-r--r--@ 1 jl staff 77K Apr 2 16:49 f001.m4a
-rw-r--r--@ 1 jl staff 39K Apr 2 16:50 f002.m4a
-rw-r--r--@ 1 jl staff 153K Apr 2 16:51 f003.m4a
-rw-r--r--@ 2 jl staff 80K Aug 15 2019 flow.jpg
-rw-r--r--@ 1 jl staff 1.0M Jan 7 18:22 fsoc.m4a
-rw-r--r--@ 1 jl staff 3.9M Jan 7 18:21 fsoc.mp4
-rw-r--r--@ 1 jl staff 10K Jan 22 19:47 macOS_bash.txt
-rw-------@ 1 jl staff 56B Jan 22 19:14 void.txt

./copy:
total 168
-rw-r--r--@ 2 jl staff 80K Aug 15 2019 flower.jpg

# Display the results in reverse order. Normally, 'ls' displays its results in ascending alphabetical order

> JLs-MacBook-Air:Terminal jl\$ ls

# Output :

copy f002.m4a flow.jpg fsoc.mp4 void.txt
f001.m4a f003.m4a fsoc.m4a macOS_bash.txt

> JLs-MacBook-Air:Terminal jl\$ ls -r

# Output :

void.txt fsoc.mp4 flow.jpg f002.m4a copy
macOS_bash.txt fsoc.m4a f003.m4a f001.m4a

# Sort files by their size

> JLs-MacBook-Air:Terminal jl\$ ls -S1

# Output :

fsoc.mp4
fsoc.m4a
f003.m4a
flow.jpg
f001.m4a
f002.m4a
macOS_bash.txt
copy
void.txt

# Display complete time information for the file, including month, day, hour, minute, second, and year.

> JLs-MacBook-Air:Terminal jl\$ ls -lT

# Output :

total 10904
drwxr-xr-x 3 jl staff 96 Apr 1 18:18:31 2020 copy
-rw-r--r--@ 1 jl staff 78778 Apr 2 16:49:37 2020 f001.m4a
-rw-r--r--@ 1 jl staff 40300 Apr 2 16:50:51 2020 f002.m4a
-rw-r--r--@ 1 jl staff 156586 Apr 2 16:51:42 2020 f003.m4a
-rw-r--r--@ 2 jl staff 82080 Aug 15 18:45:51 2019 flow.jpg
-rw-r--r--@ 1 jl staff 1098100 Jan 7 18:22:07 2020 fsoc.m4a
-rw-r--r--@ 1 jl staff 4092278 Jan 7 18:21:53 2020 fsoc.mp4
-rw-r--r--@ 1 jl staff 10394 Jan 22 19:47:31 2020 macOS_bash.txt
-rw-------@ 1 jl staff 56 Jan 22 19:14:22 2020 void.txt

# Sort by last access time & display full date & time

> JLs-MacBook-Air:Terminal jl\$ ls -lTu

# Output :

total 10904
drwxr-xr-x 3 jl staff 96 Apr 1 18:20:04 2020 copy
-rw-r--r--@ 1 jl staff 78778 Apr 2 16:49:37 2020 f001.m4a
-rw-r--r--@ 1 jl staff 40300 Apr 2 16:50:52 2020 f002.m4a
-rw-r--r--@ 1 jl staff 156586 Apr 2 16:51:42 2020 f003.m4a
-rw-r--r--@ 2 jl staff 82080 Apr 8 17:12:20 2020 flow.jpg
-rw-r--r--@ 1 jl staff 1098100 Mar 16 18:09:14 2020 fsoc.m4a
-rw-r--r--@ 1 jl staff 4092278 Mar 16 18:09:14 2020 fsoc.mp4
-rw-r--r--@ 1 jl staff 10394 Mar 16 18:24:24 2020 macOS_bash.txt
-rw-------@ 1 jl staff 56 Mar 16 18:12:53 2020 void.txt

# Use time of file creation

> JLs-MacBook-Air:Terminal jl\$ ls -lU

# Sort by version

> JLs-MacBook-Air:Terminal jl\$ ls -v

# Sort by rows rather than columns

> JLs-MacBook-Air:Terminal jl\$ ls

# Output :

copy f002.m4a flow.jpg fsoc.mp4 void.txt
f001.m4a f003.m4a fsoc.m4a macOS_bash.txt

> JLs-MacBook-Air:Terminal jl\$ ls -x

# Output :

copy f001.m4a f002.m4a f003.m4a flow.jpg
fsoc.m4a fsoc.mp4 macOS_bash.txt void.txt

# //////////////////////////// M

# ////// man

# Displays an online manual page, or manpage, for a given program.

> JLs-MacBook-Air:tutorial jl\$ man which

# ////// mkdir

# Is used to create directories. Create the directory with the given permissions (7 : read, write, execute => rwx; 5 : read & execute) :

> JLs-MacBook-Air:Terminal jl\$ mkdir -m 755 cample

# Output : /Users/jl/Terminal/cample

# Create any necessary parent directories automatically

> JLs-MacBook-Air:Terminal jl\$ mkdir -p sample/cample

# Output : (/Users/jl/Terminal/sample/cample)

# Setting permissions to Private Folder for You (6 : read & write; 0 : no rights)

> JLs-MacBook-Air:cample jl\$ mkdir -m 600 sample

# Output : /Users/jl/Terminal/cample/sample

# Be verbose when creating directories, listing them as they are created.

> JLs-MacBook-Air:Terminal jl\$ mkdir -pv 600 sample

# Output : (/Users/jl/Terminal/sample/ with 600 permission)

# ////// mkfs (make file system)

# Creates a new file system in a variety of formats.

# ////// mount

# Instructs the operating system that a file system is ready to use, and associates it with a particular point in the overall file system hierarchy (mount point) and sets options relating to its access. Mounting makes file systems, files, directories, devices and special files available for use and available to the user.

# Let's list a particular mounted device (USB) :

> kali@kali:/\$ mount | less

# /dev/sdb1 on /mnt/mydir type vfat

# Make an empty folder

> sudo mkdir /mnt/mydir

# And now let's make the directory above accessible for files on our USB :

> kali@kali:/\$ sudo mount /dev/sdb1 /mnt/mydir

> kali@kali:/\$ ls mnt/mydir

# Output : (all files listed now in our new mounted directory)

handler.pdf Intl.pdf reflect.pdf regex.pdf

# Let's show our mounted device

# /dev/sdb1 on /mnt/mydir type vfat

# ////// mv

# Renames a file & let's you move files and directories into a destination drectory :

> jl@JLs-MacBook-Air copy % mv 4_b.jpg Terminal

# Output : (The selected file gets renamed into 'Terminal')

# Now lets move the selected file in directory above :

> jl@JLs-MacBook-Air copy % mv 4_b.jpg ~/Terminal

# Force the move. If a destination file exists, overwrite it unconditionally.

> JLs-MacBook-Air:Terminal jl\$ mv -f flow.jpg ~/Terminal/empty

# Interactive mode. Ask before overwriting destination files

> JLs-MacBook-Air:Terminal jl\$ mv -fi flow.jpg ~/Terminal/empty

# Output : Deny overwriting with 'n'

overwrite /Users/jl/Terminal/empty/flow.jpg? (y/n [n]) n

not overwritten

# Do not overwrite an existing file

> JLs-MacBook-Air:Terminal jl\$ mv -n flow.jpg ~/Terminal/empty

# Output : (doesn't overwrite)

# Show files after they are being moved

> JLs-MacBook-Air:Terminal jl\$ mv -v flow.jpg ~/Terminal/empty

# Output :

flow.jpg -> /Users/jl/Terminal/empty/flow.jpg

# //////////////////////////// P

# ////// passwd

# Use the command to set or change a password. You will be prompted for your old password and your new password.

# ////// ping \*

# Tells you if a remote host is reachable. It sends small packets (ISPM packets to be precise) to a remote host and waits for responses. You can also specify how many times you want to ping some address :

> kali@kali:~\$ ping -c5 google.com

# Output :

PING google.com (172.217.19.78) 56(84) bytes of data.
64 bytes from ham02s17-in-f14.1e100.net (172.217.19.78): icmp_seq=1 ttl=63 time=15.0 ms
64 bytes from ham02s17-in-f14.1e100.net (172.217.19.78): icmp_seq=2 ttl=63 time=14.0 ms
64 bytes from ham02s17-in-f14.1e100.net (172.217.19.78): icmp_seq=3 ttl=63 time=10.7 ms
64 bytes from ham02s17-in-f14.1e100.net (172.217.19.78): icmp_seq=4 ttl=63 time=11.5 ms
64 bytes from ham02s17-in-f14.1e100.net (172.217.19.78): icmp_seq=5 ttl=63 time=11.5 ms

--- google.com ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4134ms
rtt min/avg/max/mdev = 10.727/12.535/14.971/1.632 ms

# ////// printenv \*

# Lists a shell's environment variables

> JLs-MacBook-Air:tutorial jl\$ printenv

# Output :

TERM*PROGRAM=Apple_Terminal
SHELL=/bin/bash
TERM=xterm-256color
TMPDIR=/var/folders/mv/qvqj3nf51yqd4x7jq4kbym7h0000gn/T/
TERM_PROGRAM_VERSION=433
OLDPWD=/Users/jl/Shell/code
TERM_SESSION_ID=CEEEFD44-1909-457F-89C7-E8E21043E41D
USER=jl
SSH_AUTH_SOCK=/private/tmp/com.apple.launchd.5utpTDhvBR/Listeners
PATH=/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
PWD=/Users/jl/Shell/code/tutorial
XPC_FLAGS=0x0
XPC_SERVICE_NAME=0
SHLVL=1
HOME=/Users/jl
LOGNAME=jl
LC_CTYPE=UTF-8
*=/usr/bin/printenv

# ////// ps \*

# Displays information about your running processes, and optionally the processes of other users :

> JLs-MacBook-Air:empty jl\$ ps

# Output (It lists single process 984 which is bash):

PID TTY TIME CMD
984 ttys004 0:00.18 -bash

# Show all of our processes regardless of what terminal (if any) they are controlled by.

> JLs-MacBook-Air:~ jl\$ ps x

# Output (Legend of the Process States in Notes) :

PID TT STAT TIME COMMAND
315 ?? S 0:00.14 /System/Library/Frameworks/LocalAuthentication.frame
316 ?? S 0:01.20 /usr/sbin/cfprefsd agent
320 ?? S 0:00.96 /usr/libexec/UserEventAgent (Aqua)
322 ?? S 0:00.58 /usr/sbin/distnoted agent
323 ?? S 0:00.37 /usr/sbin/universalaccessd launchd -s
...

625 s000 Ss 0:00.05 login -pf jl
626 s000 S 0:00.04 -bash
682 s000 R+ 0:00.01 ps x

# Display information about other users' processes, including those without controlling terminals

> JLs-MacBook-Air:empty jl\$ ps -A

# Output (? indicates no controlling terminal):

PID TTY TIME CMD
1 ?? 0:09.93 /sbin/launchd
88 ?? 0:00.75 /usr/sbin/syslogd
89 ?? 0:03.84 /usr/libexec/UserEventAgent (System)
91 ?? 0:00.31 /System/Library/PrivateFrameworks/Uninstall.framework/Res
92 ?? 0:02.47 /usr/libexec/kextd
93 ?? 0:06.24 /System/Library/Frameworks/CoreServices.framework/Version
95 ?? 0:00.37 /System/Library/PrivateFrameworks/MediaRemote.framework/S
98 ?? 0:02.30 /usr/sbin/systemstats --daemon
99 ?? 0:01.81 /usr/libexec/configd
...

1204 ?? 0:00.60 /Applications/Firefox.app/Contents/MacOS/plugin-container
983 ttys004 0:00.04 login -pf jl
984 ttys004 0:00.23 -bash
1207 ttys004 0:00.00 ps -A

# Display the processes belonging to every user.

> JLs-MacBook-Air:~ jl\$ ps aux

# Output (USER -> User ID. This is the owner of the process;

# %CPU -> CPU usage in percent

# %MEM -> Memory usage in percent

# VSZ -> Virtual memory size

# RSS -> Resident set size. This is the amount of physical memory (RAM) the process is using in kilobytes

# START -> Time when the process started. For values over 24 hours, a date is used)

> USER PID %CPU %MEM VSZ RSS TT STAT STARTED TIME COMMAND
> \_windowserver 221 2.0 1.0 6585512 42924 ?? Ss 3:22PM 10:27.58 /System/Library/
> jl 969 1.9 1.0 4944028 43128 ?? S 4:09PM 1:00.12 /System/Applicat
> \_hidd 143 1.5 0.2 4336428 7068 ?? Ss 3:22PM 2:03.99 /usr/libexec/hid
> root 101 0.1 0.1 4334896 5876 ?? Ss 3:22PM 0:08.19 /System/Library/

# ////// pstree

# Outputs a process list arranged in a tree-like pattern showing the parent-child relationships between processes

> kali@kali:~\$ pstree

# Output :

systemd─┬─ModemManager───2*[{ModemManager}]
├─NetworkManager───2*[{NetworkManager}]
├─2*[VBoxClient───VBoxClient]
├─2*[VBoxClient───VBoxClient───2*[{VBoxClient}]]
├─VBoxClient───VBoxClient───3*[{VBoxClient}]
├─VBoxService───8*[{VBoxService}]
├─agetty
├─colord───2*[{colord}]
├─cron
├─dbus-daemon
├─haveged
├─lightdm─┬─Xorg───5*[{Xorg}]
│ ├─lightdm─┬─xfce4-session─┬─Thunar───2*[{Thunar}]
│ │ │ ├─agent───2*[{agent}]
│ │ │ ├─applet.py
│ │ │ ├─light-locker───3*[{light-locker}]
│ │ │ ├─nm-applet───3*[{nm-applet}]
│ │ │ ├─polkit-gnome-au───2*[{polkit-gnome-au}]
│ │ │ ├─ssh-agent
│ │ │ ├─xfce4-panel─┬─panel-1-whisker───2*[{pan+
│ │ │ │ ├─panel-15-systra───2*[{pan+
│ │ │ │ ├─panel-16-pulsea───2*[{pan+
│ │ │ │ ├─panel-17-notifi───2*[{pan+
│ │ │ │ ├─panel-18-power-───2*[{pan+
│ │ │ │ ├─panel-20-action───2*[{pan+
│ │ │ │ └─2*[{xfce4-panel}]
│ │ │ ├─xfdesktop───2*[{xfdesktop}]
│ │ │ ├─xfwm4───6*[{xfwm4}]
│ │ │ ├─xiccd───2*[{xiccd}]
│ │ │ └─2*[{xfce4-session}]
│ │ └─2*[{lightdm}]
│ └─2*[{lightdm}]
├─polkitd───2*[{polkitd}]
├─qterminal─┬─bash───pstree
│ └─6*[{qterminal}]
├─rsyslogd───3*[{rsyslogd}]
├─rtkit-daemon───2*[{rtkit-daemon}]
├─smartd
├─systemd─┬─(sd-pam)
│ ├─at-spi-bus-laun─┬─dbus-daemon
│ │ └─3*[{at-spi-bus-laun}]
│ ├─at-spi2-registr───2*[{at-spi2-registr}]
│ ├─dbus-daemon
│ ├─dconf-service───2*[{dconf-service}]
│ ├─gpg-agent
│ ├─gvfs-udisks2-vo───3*[{gvfs-udisks2-vo}]
│ ├─gvfsd─┬─gvfsd-trash───2*[{gvfsd-trash}]
│ │ └─2*[{gvfsd}]
│ ├─gvfsd-metadata───2*[{gvfsd-metadata}]
│ ├─pulseaudio───2*[{pulseaudio}]
│ ├─xfce4-notifyd───2*[{xfce4-notifyd}]
│ └─xfconfd───2*[{xfconfd}]
├─systemd-journal
├─systemd-logind
├─systemd-udevd
├─udisksd───4*[{udisksd}]
├─upowerd───2*[{upowerd}]
├─xcape───{xcape}
├─xfce4-power-man───2*[{xfce4-power-man}]
└─xfsettingsd───2\*[{xfsettingsd}]

# ////// pwd (print working directory)

# Displays the current working directory

# //////////////////////////// R

# ////// rm

# Deletes files or directories. Force the deletion, ignoring any errors or warnings

> JLs-MacBook-Air:del jl\$ rm -f \*.png

# Output : (deletes all (3 in this case) files of .png format)

# Interactive mode. Ask before deleting each file

> JLs-MacBook-Air:del jl\$ rm -i \*.png

# Output :

remove Screenshot 2020-04-06 at 19.11.50.png? n
remove Screenshot 2020-04-06 at 19.12.22.png? n
remove Screenshot 2020-04-06 at 19.13.49.png? n

# Attempt to remove directories as well as other types of files. Does work if the folder is empty

> JLs-MacBook-Air:del jl\$ rm -di empty

# Output : (deletes folder)

remove empty? y

# Recursively remove a directory and its contents. Use with caution, especially if combined with the -f option, as it can wipe out all your files

> JLs-MacBook-Air:del jl\$ rm -fr \*

# Output : (wipes everything, use )

# //////////////////////////// S

# ////// script

# Is used to record an entire shell session and store it in a file. If no file is specified, the file 'typescript' is used. Following example uses 'void.txt' file as a storing for the recordings.

> [JLs-MacBook-Air:tutorial] jl\$ script void.txt

# ////// shutdown

# Halts or reboots a Linux system; only the superuser may run it. Let's power the system of :

> kali@kali:~\$ sudo shutdown -P

# Output : (after some time the system shuts off)

# Cancel the pending shutdown :

> kali@kali:~\$ sudo shutdown -c

# Reboot the machine :

> kali@kali:~\$ sudo shutdown -r

# ////// su

# Is used to start a shell as another user. Doesn't work on Mac.

# ////// sudo

# Allows a permitted user to execute a command as the superuser or another user, as specified by the security policy. One special user, called the superuser or root, has full access to the machine and can do anything on it.

# //////////////////////////// T

# ////// tail

# It's similiar to 'head' command only it prints the last n lines. Using example from 'grep' command :

> JLs-MacBook-Air:tutorial jl\$ tail -n 5 void.txt

# Output : (1st & last lines count as 2)

duku

vintar

# Keep the file open, and whenever lines are appended to the file, print them. But 1st let's print two last lines of the log messages :

> kali@kali:~\$ sudo tail -f /var/log/messages

# Output :

Apr 24 16:16:20 kali org.freedesktop.thumbnails.Thumbnailer1[1126]: Registered thumbnailer /usr/bin/gdk-pixbuf-thumbnailer -s %s %u %o
Apr 24 16:16:20 kali org.freedesktop.thumbnails.Thumbnailer1[1126]: Registered thumbnailer /usr/bin/gdk-pixbuf-thumbnailer -s %s %u %o

# After we plug a USB device :

Apr 24 16:16:20 kali org.freedesktop.thumbnails.Thumbnailer1[1126]: Registered thumbnailer /usr/bin/gdk-pixbuf-thumbnailer -s %s %u %o
Apr 24 16:19:17 kali kernel: [ 198.479319] usb 1-1: new high-speed USB device number 2 using ehci-pci
Apr 24 16:19:17 kali kernel: [ 198.531815] usb 1-1: New USB device found, idVendor=058f, idProduct=6387, bcdDevice= 1.01
Apr 24 16:19:17 kali kernel: [ 198.531819] usb 1-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
Apr 24 16:19:17 kali kernel: [ 198.531821] usb 1-1: Product: Mass Storage
Apr 24 16:19:17 kali kernel: [ 198.531823] usb 1-1: Manufacturer: Generic
Apr 24 16:19:17 kali kernel: [ 198.531824] usb 1-1: SerialNumber: A8BB570B
Apr 24 16:19:17 kali kernel: [ 198.566037] usb-storage 1-1:1.0: USB Mass Storage device detected
Apr 24 16:19:17 kali kernel: [ 198.568781] scsi host3: usb-storage 1-1:1.0
Apr 24 16:19:17 kali kernel: [ 198.568873] usbcore: registered new interface driver usb-storage
Apr 24 16:19:17 kali kernel: [ 198.572781] usbcore: registered new interface driver uas
Apr 24 16:19:18 kali kernel: [ 199.666075] scsi 3:0:0:0: Direct-Access Generic Flash Disk 8.07 PQ: 0 ANSI: 2
Apr 24 16:19:18 kali kernel: [ 199.666726] scsi 3:0:0:0: Attached scsi generic sg2 type 0
Apr 24 16:19:18 kali kernel: [ 199.693295] sd 3:0:0:0: [sdb] 2068480 512-byte logical blocks: (1.06 GB/1010 MiB)
Apr 24 16:19:18 kali kernel: [ 199.701569] sd 3:0:0:0: [sdb] Write Protect is off
Apr 24 16:19:18 kali kernel: [ 199.776733] sdb: sdb1
Apr 24 16:19:18 kali kernel: [ 199.813735] sd 3:0:0:0: [sdb] Attached SCSI removable disk

# ////// tee

# Reads standard input and copies it to both standard output (allowing the data to continue down the pipeline) and to one or more files. This is useful for capturing a pipeline's contents at an intermediate stage of processing

# Let's repeat our 'grep' example and by doing this print out words wich contain 'on' to 'v01.txt' file

> JLs-MacBook-Air:tutorial jl\$ less void.txt | tee ~/Shell/v01.txt | grep on

sonne
alfones

# Now let's append instead of overwriting files. Make sure that in the end you have 'less' or else it gets printed right in terminal.

> JLs-MacBook-Air:del jl\$ less type.txt | tee -a inp.txt | less

# Output : (the output gets appended to the .txt file)

# ////// top

# Let's you monitor the most active processes, updating the display at regular intervals (say, every second). It is a screen-based program that updates the display in place, interactively

# ////// touch

# Changes two timestamps associated with a file: its modification time (when the file's data was last changed) and its access time (when the file was last read). To set both timestamps (and create a new file btw) to right now, run:

> kali@kali:~/shell$ touch foo.txt
> kali@kali:~/shell$ ls -l foo.txt

# Output :

-rw-r--r-- 1 kali kali 0 Apr 27 16:46 foo.txt

# You can set these timestamps to arbitrary values, for example

> kali@kali:~/shell$ touch -d "November 18 1975" foo.txt
> kali@kali:~/shell$ ls -l foo.txt
> -rw-r--r-- 1 kali kali 0 Nov 18 1975 foo.txt

# Change the modification time only

> kali@kali:~/shell$ touch -m foo.txt
> kali@kali:~/shell$ ls -l foo.txt

# Output (changes from 1975 to present time) :

-rw-r--r-- 1 kali kali 0 Apr 27 17:02 foo.txt

# If the file doesn't exist, don't create it (normally, touch creates it)

> kali@kali:~/shell$ touch -c fool.txt
> kali@kali:~/shell$ ls -l fool.txt

# Output :

ls: cannot access 'fool.txt': No such file or directory

# ////// traceroute

# Prints the network path from your local host to a remote host, and the time it takes for packets to traverse the path :

> kali@kali:~\$ traceroute yandex.ru

Output :

traceroute to yandex.ru (77.88.55.66), 30 hops max, 60 byte packets
1 10.0.2.2 (10.0.2.2) 0.666 ms 0.642 ms 0.622 ms
2 fritz.box (192.168.178.1) 2.549 ms 2.728 ms 2.866 ms
3 \* \* \*
4 v1204.b690.Ernie.ipv4.wtnet.de (84.46.105.85) 19.890 ms 20.199 ms 21.919 ms
5 b203.Bibo.ipv4.wtnet.de (84.46.112.69) 25.695 ms 27.145 ms 28.259 ms
6 b31040.Kermit.ipv4.wtnet.de (84.46.113.253) 28.833 ms 23.873 ms 24.181 ms
7 ams-ix-am1.yandex.net (80.249.211.200) 25.146 ms 22.160 ms 25.009 ms
8 yandex.ru (77.88.55.66) 50.099 ms 48.329 ms 51.187 ms

# ////// type

# // Is a shell builtin that displays the kind of command the shell will execute, given a particular command name. Following example shows character 'c' being aliased for command 'clear'

> jl@JLs-MacBook-Air copy % type c

# Output : c is an alias for clear

> jl@JLs-MacBook-Air copy % type alias

# Output : alias is a shell builtin

# //////////////////////////// U

# ////// umask

# Controls the default permissons given to a file when it is created. 1st we delete everything and set the mask to its full potential :

> JLs-MacBook-Air:empty jl\$ rm -rf \*

> JLs-MacBook-Air:empty jl\$ umask 0000

# Then we create a file like this :

> JLs-MacBook-Air:empty jl\$ > f.txt

# ... and display its permissions

> JLs-MacBook-Air:empty jl\$ ls -l

# Output :

total 0
-rw-rw-rw- 1 jl staff 0 Apr 15 20:11 f.txt

# If you create a new folder it will look like this (v is a folder):

drwxrwxrwx 2 jl staff 64 Apr 15 20:11 v

# Now you can set your new mask to 0002 (000 000 000 010) :

> JLs-MacBook-Air:empty jl\$ rm -rf \*

> JLs-MacBook-Air:empty jl\$ umask 0002

> JLs-MacBook-Air:empty jl\$ > f.txt

> JLs-MacBook-Air:empty jl\$ mkdir v

JLs-MacBook-Air:empty jl\$ ls -l

# Output : (Because of 1 in 010 it unsets the value which in our case is 'w' for everyone)

total 0
-rw-rw-r-- 1 jl staff 0 Apr 15 20:22 f.txt
drwxrwxr-x 2 jl staff 64 Apr 15 20:22 v

# ////// umount

# Detaches the mentioned file system(s) from the file hierarchy. A file system is specified by giving the directory where it has been mounted. So overall it makes a disk partition unavailable via the filesystem.

# ////// uniq

# Accepts a sorted list of data from either standard input and, by default, removes any duplicates from the list. In example below we have some random unsorted letters :

duku

sonne

zenit

alfones

petro

valiant

duku

zenit

vintar

# Let's sort them alphabetically and remove repeat lines

> JLs-MacBook-Air:tutorial jl\$ less v01.txt | sort | uniq | less

# Output :

alfones
duku
petro
sonne
valiant
vintar
zenit

# Let's print only sorted duplicate lines

> JLs-MacBook-Air:tutorial jl\$ less v01.txt | sort | uniq -d | less

# Output :

duku
zenit

# Count adjacent duplicate lines

> JLs-MacBook-Air:Shell jl\$ less v01.txt | sort | uniq -c | less

# Output : (9 words overall in the list)

9
1 alfones
2 duku
1 petro
1 sonne
1 valiant
1 vintar
2 zenit

# Print unique lines only

> less v01.txt | sort | uniq -u | less

# Output :

alfones
petro
sonne
valiant
vintar

# //////////////////////////// V

# ////// vmstat

# Output a snapshot of system resource usage including memory, swap, and disk I/O.

> kali@kali:~\$ vmstat

# Output :

procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
r b swpd free buff cache si so bi bo in cs us sy id wa st
0 0 0 1266148 39976 329704 0 0 90 2 58 121 1 0 99 0 0

FIELD DESCRIPTION FOR VM MODE

Procs
r: The number of runnable processes (running or waiting for run time).
b: The number of processes in uninterruptible sleep.

Memory
These are affected by the --unit option.
swpd: the amount of virtual memory used.
free: the amount of idle memory.
buff: the amount of memory used as buffers.
cache: the amount of memory used as cache.
inact: the amount of inactive memory. (-a option)
active: the amount of active memory. (-a option)

Swap
These are affected by the --unit option.
si: Amount of memory swapped in from disk (/s).
so: Amount of memory swapped to disk (/s).

IO
bi: Blocks received from a block device (blocks/s).
bo: Blocks sent to a block device (blocks/s).

System
in: The number of interrupts per second, including the clock.
cs: The number of context switches per second.

CPU
These are percentages of total CPU time.
us: Time spent running non-kernel code. (user time, including nice time)
sy: Time spent running kernel code. (system time)
id: Time spent idle. Prior to Linux 2.5.41, this includes IO-wait time.
wa: Time spent waiting for IO. Prior to Linux 2.5.41, included in idle.
st: Time stolen from a virtual machine. Prior to Linux 2.6.11, unknown.

# //////////////////////////// W

# ////// wc

# Is used to display the number of lines (0-indexed), words, and bytes contained in files (space counts for 2 bytes). Let's apply it to the file containing following:

duku

zenit

> JLs-MacBook-Air:tutorial jl\$ less void.txt | wc

# Ouput :

3 2 12

# ////// wget

# Captures a URL and downloads the data to a file or standard output. It supports HTTP, HTTPS, and FTP protocols, as well as retrieval through HTTP proxies. It's great for capturing individual web pages, downloading files, or duplicating entire website hierarchies to arbitrary depth.

> kali@kali:~\$ wget bit.ly/3aMrz8p

# Output (saving some pdf file) :

--2020-04-28 09:44:13-- http://bit.ly/3aMrz8p
Resolving bit.ly (bit.ly)... 67.199.248.10, 67.199.248.11
Connecting to bit.ly (bit.ly)|67.199.248.10|:80... connected.
HTTP request sent, awaiting response... 301 Moved Permanently
Location: https://www.modelwerk.de/pdf/sedcard/Anis_Ben_Choug.pdf?id=5830 [following]
--2020-04-28 09:44:13-- https://www.modelwerk.de/pdf/sedcard/Anis_Ben_Choug.pdf?id=5830
Resolving www.modelwerk.de (www.modelwerk.de)... 35.189.198.49
Connecting to www.modelwerk.de (www.modelwerk.de)|35.189.198.49|:443... connected.
HTTP request sent, awaiting response... 200
Length: unspecified [application/pdf]
Saving to: ‘3aMrz8p’

3aMrz8p [ <=> ] 2.02M 6.36MB/s in 0.3s

2020-04-28 09:44:14 (6.36 MB/s) - ‘3aMrz8p’ saved [2120744]

# -c : Continue mode which is added ability to resume a download if it gets interrupted in the middle, say, due to a network failure: just run wget -c with the same URL and it picks up where it left off

# //////////////////////////// X

# ////// xargs

# Reads lines of text from standard input, turns them into commands, and executes them. Here we use the find command piped into xargs, which, in turn, constructs an argument list for the ls command and then executes it :

> kali@kali:~\$ find ~ -type f -name 'foo\*' -print | xargs ls -l

# Output :

-rw-r--r-- 1 kali kali 0 Apr 27 17:07 /home/kali/shell/foo.txt

////////////////////////////////////////////////////////////

# G

# ///////////// grep

Is a powerful program used to find text patterns within files. It's used like this

> `>` grep _pattern_ _filename_

When
