# LinuxTraining
The computer programs that allocate system resources and coordinate all the details of the computer's internals is called the operating system or the kernel.
Users communicate with the kernel through a program known as the shell.
The shell is command line interpreter it translates commands entered by the user
and converts them into a language that is understood by the Kernel.


Several People can be use Unix or Linux computer at the same time . So unix or Linux is called a multi user system

a user can also run multiple programs at the same time hence these operating systems are called as Multi tasking operating systems


Kernel:
 The Kernel is the heart of the operating system. It interacts with the hardware and most of the tasks like memory management, task scheduling and file management.


Shell:

The Shell is the utility that process your requests. When we type commands at the terminal the shell interprets the command and calls the program that we want. The shell uses standard syntax.


Commands and Utilities:

There are over 250 standard commands plus numerous others provided through 3rd party software. All the commands come along with various options
ex: cp,mv,cat, grep

$ls

To list the files and directories stored in the current directory.

$ls -l

we used to get more information about the listed files.

Metacharacters:

Metacharacters have a special meaning in Unix. For example, * and ? are metacharacters. We use * to match 0 or more characters, a question mark (?) matches with a single character.


$ls ch*.doc
Displays all the files, the names of which start with ch and end with .doc−

Here,* works as metacharacter which matches with any character. If you want to display all the files ending with just .doc, then you can use the following command.
$ls *.doc


$ ls *.rb
name.rb trelloex1.rb

Single dot (.)− This represents the current directory.
Double dot (..)− This represents the parent directory.
Creating Files:
We can use use the vi editor to create ordinary files on any Unix system
$vi filename

The above command will open a file with the given filename. Now, press the key i to come into the edit mode. Once you are in the edit mode
Once you are done with the program, follow these steps −

	Press 	the key esc to come out of the edit mode.
	Press 	two keys Shift + ZZ together to come out of the file 	completely.

Or we can use
esc then :wq for saving file
or
esc :q!
For not changing any modifications.




Vi filename
once file open we used for navigation
h key to move to left side
j key to move down side the file
k key to move upside the file.
L key to move right side.

Display Content of a File:

We can use the cat command to see the content of a file.

$ cat filename
we can display the line numbers by using the -b option along with the cat command

$ cat -b filename

counting words:

we can use the wc command to get a count of the total number of lines, words, and characters contained in a file

$ wc filename
ex: $ wc soft
2  19 103 filename



We can give multiple files and get information about those files at a time. Following is simple syntax −

$ wc filename1 filename2 filename3

bhagath@adminpc-ThinkPad-T520:~$ wc exss software
11 5 90 exss
2 5 24 software
13 10 114 total




copying files:
to make a copy of a file use cp command. The basic syntax
$ cp source_file destination_file
$ cp filename copyfile
we will now find one more file copyfile in your current directory. This file will exactly be the same as the original file filename.
ex:


bhagath@adminpc-ThinkPad-T520:~$ cat software
ldkfjaoifjafkkkn
jfa iu4ewfrw
hfdahfoikkhh
bhagath@adminpc-ThinkPad-T520:~$ cp software doft
bhagath@adminpc-ThinkPad-T520:~$ cat doft
ldkfjaoifjafkkkn
jfa iu4ewfrw
hfdahfoikkhh


---------------------
Renaming Files


To change the name of a file, use the mv command. Following is the basic syntax −
$ mv old_file new_file
The following program will rename the existing file filename to newfile.
$ mv filename newfile
$


The mv command will move the existing file completely into the new file. In this case, you will find only newfile in your current directory.
Ex:
bhagath@adminpc-ThinkPad-T520:~$ mv doft softex1
bhagath@adminpc-ThinkPad-T520:~$ cat doft
cat: doft: No such file or directory
bhagath@adminpc-ThinkPad-T520:~$ ls *doft
ls: cannot access '*doft': No such file or directory
bhagath@adminpc-ThinkPad-T520:~$ cat softex1
ldkfjaoifjafkkkn
jfa iu4ewfrw
hfdahfoikkhh


Deleting Files
To delete an existing file, use the rm command. Following is the basic syntax −
$ rm filename
Caution − A file may contain useful information. It is always recommended to be careful while using this Delete command. It is better to use the -i option along with rm command.
Following is the example which shows how to completely remove the existing file filename.
$ rm filename
$
You can remove multiple files at a time with the command given below −
$ rm filename1 filename2 filename3
$


ex:
bhagath@adminpc-ThinkPad-T520:~$ rm softex1
bhagath@adminpc-ThinkPad-T520:~$ cat softex1
cat: softex1: No such file or directory
bhagath@adminpc-ThinkPad-T520:~$ rm software exss




pwd to print the current working directory

$ pwd

we can go in home directory anytime using the command
$ cd

Directories are created by using command

$ mkdir dirname

Changing directory

$ cd dirname

Removing Directory

$rmdir dirname
we can remove multiple directories at a time as follows −
$rmdir dirname1 dirname2 dirname3


Renaming Directories
The mv (move) command can also be used to rename a directory. The syntax is as follows
To go in your last directory, you can use the following command

$ ls dirname

ex:
bhagath@adminpc-ThinkPad-T520:~/projects/exampleapp$ ls app
assets helpers mailers controllers models views


Stopping Processes:

If a process is running in the background, you should get its Job ID using the ps command. After that, you can use the kill command to kill the process

$ps -f


the kill command terminates the first_one process. If a process ignores a regular kill command, you can use kill -9 followed by the process ID as follows −
$kill -9 6738
Terminated




The top command
shows information about physical and virtual memory, CPU usage, load averages, and your busy processes.

$top





The ping Utility
The ping command sends an echo request to a host available on the network. Using this command, you can check if your remote host is responding well or not.
The ping command is useful for the following −
Tracking and isolating hardware and software problems.
Determining the status of the network and various foreign hosts.
Testing, measuring, and managing networks.
Syntax
$ping hostname or ip-address


$ ping google.com

Ex:
$ ping 192.168.2.31


VI Editor:

a look at VI and nano text Editors

nano is much easy

vi myfile

type i that is insert mode

:wq!
Save and close

:q!
closes without saving

hit esc and hit u key thats do undo
:w! save file without closing

vi filename
Creates a new file if it already does not exist, otherwise opens an existing file.
vi -R filename
Opens an existing file in the read-only mode.

Operation Modes
Command mode
Insert mode
vi always starts in the command mode. To enter text, you must be in the insert mode for which simply type i. To come out of the insert mode, press the Esc key, which will take you back to the command mode.
commands we can use to move around one character at a time
K Moves the cursor up one line
j Moves the cursor down one line
h Moves the cursor to the left one character position
l Moves the cursor to the right one character position


Most commands in vi can be prefaced by the number of times you want the action to occur. For example,2j moves the cursor two lines down the cursor location.

Expansion:

$ echo this is a test
this is a test

PathName Expansion:
$ echo *

Desktop Documents ls-outp
$ echo D*

Desktop Documents
$echo *ss
Documents Pictures Templates Videos

$ echo [[:upper:]]*
Desktop Documents Music Pictures Public Templates Videos

Tilde Expansion


the tilde character (“~”) has a special meaning. When used at the beginning of a word, it expands into the name of the home directory of the named user, or if no user is named, the home directory of the current user


$ echo ~
/home/bhagath
$echo ~bhagathho ~foo
/home/bhagath
Arithmetic Expansion

$ echo $((2+2))
4

Arithmetic expansion uses the form:
       $((expression))

to multiply five squared by three:

$ echo $(($((5**2)) * 3))
75
we can rewrite the example above and get the same result using a single expansion instead of two:

$ echo $((5**2)*3))
75
Parameter Expansion

the variable named “USER” contains your user name. To invoke parameter expansion and reveal the contents of USER you would do this:
$ echo $USER
bhagath
to see a list of available variables try like below cmd.
$ printenv | less
Command Substitution
$ echo $(ls)
attr_reader.rb initialize_method_use.rb module_function.rb module.rb problem2
$ ls -l $(which cp)
-rwxr-xr-x 1 root root 151024 Feb 18 2016 /bin/cp
Command substitution allows us to use the output of a command as an expansion:


Quoting:
$ echo The total is $100.00
The total is 00.00
$ echo this is a test
this is a test


$ echo “this is a test”
this is a test


$ echo "$USER $((2+2)) $(cal)"
bhagath 4 June 2017
Su Mo Tu We Th Fr Sa
1 2 3
4 5 6 7 8 9 10
11 12 13 14 15 16 17
18 19 20 21 22 23 24
25 26 27 28 29 30
$ echo $(cal)
June 2017 Su Mo Tu We Th Fr Sa 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 190 21 22 23 24 25 26 27 28 29 30


Job Control:

There are several commands that can be used to control processes. They are:

ps
kill
jobs
bg
fg

xload which displays a graph representing system load
$ xload
$ xload &
[1] 17478

 kill -l

will give you a list of the signals it supports. Most are rather obscure, but several(4) are useful to know:
1) SIGHUP	 2) SIGINT 9)SIGKILL 15)SIGTERM


$ kill -l
1) SIGHUP	 2) SIGINT	 3) SIGQUIT	 4) SIGILL	 5) SIGTRAP
6) SIGABRT	 7) SIGBUS	 8) SIGFPE	 9) SIGKILL	10) SIGUSR1
11) SIGSEGV	12) SIGUSR2	13) SIGPIPE	14) SIGALRM	15) SIGTERM
16) SIGSTKFLT	17) SIGCHLD	18) SIGCONT	19) SIGSTOP	20) SIGTSTP
21) SIGTTIN	22) SIGTTOU	23) SIGURG	24) SIGXCPU	25) SIGXFSZ
26) SIGVTALRM	27) SIGPROF	28) SIGWINCH	29) SIGIO	30) SIGPWR
31) SIGSYS	34) SIGRTMIN	35) SIGRTMIN+1	36) SIGRTMIN+2	37) SIGRTMIN+3
38) SIGRTMIN+4	39) SIGRTMIN+5	40) SIGRTMIN+6	41) SIGRTMIN+7	42) SIGRTMIN+8
43) SIGRTMIN+9	44) SIGRTMIN+10	45) SIGRTMIN+11	46) SIGRTMIN+12	47) SIGRTMIN+13
48) SIGRTMIN+14	49) SIGRTMIN+15	50) SIGRTMAX-14	51) SIGRTMAX-13	52) SIGRTMAX-12
53) SIGRTMAX-11	54) SIGRTMAX-10	55) SIGRTMAX-9	56) SIGRTMAX-8	57) SIGRTMAX-7
58) SIGRTMAX-6	59) SIGRTMAX-5	60) SIGRTMAX-4	61) SIGRTMAX-3	62) SIGRTMAX-2
63) SIGRTMAX-1	64) SIGRTMAX

Killing Process

$ps x | grep rails

$ kill pid


kill 2932




Writing shell script:

A shell script is a file that contains ASCII text. To create a shell script, we use a text editor. A text editor is a program, like a word processor, that reads and writes ASCII text files. There are many, many text editors available for your Linux system, both for the command line environment and the GUI environment
Text Editors:
vi, vim
viis powerful, lightweight, and fast. Learning vi is a Unix rite of passage, since it is universally available on Unix-like systems. On most Linux distributions, an enhanced version of the traditional vi editor called vim is used.


Nano:
nano is very easy to use but short on features.nano for first time users who need a command line editors


gedit:
gedit is the editor supplied with the Gnome desktop environment




Strems pipes, Redirects, & Grep!

wc,split,cat, and diff


cat used concatinate and combine and display the entire file
$ cat file2
$ cat file1 file2

cat file*
$ ls -al
$ wc
$ cat file * | wc -l
$ cat file *

man command is used for knowing information about commands
ex:
$ man wc

split command.

$ cat testfile
Hyderaba
test1
tts
gsaj

$ split -l 2 testfile

$ cat xaa
Hyderaba
test1
$ cat xab
tts


Diff command

finding difference bitween 2 files

$ diff xab xac

finding Files

which Whereis commands

which command allows us to see the full path of shell command
 $ which showlog
 show the full Path

 $ which ls
 /bin/ls
$ which cp
 /bin/cp
 $ which pwd
 /bin/pwd
 $ /bin/pwd
  /home/bhagath/LinuxTraining/LinuxTraining

  inside our shell terminal whenever we log into terminal the variable is set

  we navigate the bin directory we can find lot of commonds

 $ echo $PATH
 display the PATH



 whereis command
binary location of page display

$ whereis pwd
pwd: /bin/pwd /usr/include/pwd.h /usr/share/man/man1/pwd.1.gz


Locate
find files by name.
locate  reads  one or more databases prepared by updatedb(8) and writes file names matching at least one of the PATTERNs to standard output, one per line

$ locate 22683.docx
/home/bhagath/Downloads/22683.docx

in some systems not available so we need to check whether it is installed or not using below command

$ which locate
/usr/bin/locate

$ locate kernel | grep /user
/lib/modules/4.4.0-21-generic/kernel/drivers/input/serio/userio.ko
/lib/modules/4.4.0-21-generic/kernel/drivers/regulator/userspace-consumer.ko
/lib/modules/4.4.0-71-generic/kernel/drivers/input/serio/userio.ko
/lib/modules/4.4.0-71-generic/kernel/drivers/regulator/userspace-consumer.ko
/lib/modules/4.4.0-72-generic/kernel/drivers/input/serio/userio.ko

Find command

the powerful command
find - search for files in a directory hierarchy
5
search files

search directories
search files which has modified last day.
search file  based on size.
search files which has last accessed one day.


$ find .
$ find . -name 'cron*'

$ find . -name 'cron'

$ find . -type f -name 'testfirst*'

$ find . -type d -name 'cron*'

$ find . -type d -name 'LinuxTraining'

find las modified files using below command

$ find / -mtime +1

$ find / -atime +1
cd
$ find . -size 512c
$ find . -size 1024c



$ touch astil1
$ touch astil2
$ ls
astil1  astil2  README.md  testfirst
$ chmod 777 astil1
$ chmod 555 astil2
$ find astil1
astil1
$ find astil2
astil2
$ find -perm 777
./astil1
$ find -perm 555
./astil2

we can change the permission of a file

$ find -perm 777 -exec chmod 555 {} \;
$ find -perm 555
./astil1
./astil2
$ find -perm 777
$

finding  files as a group name
$ find / -group nameofgroup

$ find . -name 'astil*';
./astil1
./astil2

$ ls
astil1  astil2  README.md  testfirst
$ find . -name 'astil*' -exec rm {} \;
rm: remove write-protected regular empty file './astil1'? y
rm: remove write-protected regular empty file './astil2'? y
$ ls
README.md  testfirst

the above command is very useful when Changing permissions Changing ownerships Removing empty files.

Streams:

Streams is basically nothing but what is displaying on Linux terminal screen

standard input
standard output
standard error

ex:
$ ls
astil1  astil2  README.md  testfirst
$ ls dlsfjoioifaog
ls: cannot access 'dlsfjoioifaog': No such file or directory

standard input is whatever input we type in the  terminal(command line)

$ echo "tester"
tester

$ echo "tester" > testtexst
$ ls
astil1  astil2  newfile  README.md  testfirst  testtexst
$ cat testtexst
tester


$ echo "testing file" > filename
$ cat filename
testing file
$ echo "my new entry" > filename
$ cat filename
my new entry
$ echo "my new entry" >> filename
$ echo "my new entry" >> filename
$ echo "my new entry" >> filename
$ cat filename
my new entry
my new entry
my new entry
my new entry
$ echo "my  entry" > filename
$ cat filename
my  entry

Standard Input
The standard input stream typically carries data from a user to a program. Programs that expect standard input usually receive input from a device, such as a keyboard. Standard input is terminated by reaching EOF (end-of-file). As described by its name, EOF indicates that there is no more data to be read.
To see standard input in action, run the cat program. Cat stands for concatenate, which means to link or combine something. It is commonly used to combine the contents of two files. When run on its own, cat opens a looping prompt.


After opening cat, type a series of numbers as it is running.
$ cat
1
1
2
2
ctrl d

$ echo Sent to the terminal through standard output
Sent to the terminal through standard output
$ echo

Pipes:

$ ls /etc | grep cron
anacrontab
cron.d
cron.daily
cron.hourly
cron.monthly
crontab
cron.weekly

$ ls /etc | grep cron | grep cron.daily
cron.daily

$ ls /etc | grep cron | grep cron.daily > grep.txt
$ cat grep.txt
cron.daily

for displating in sorted order
$ ls /etc | sort -f

$ ls /etc | sort -f > sorted.txt

$ cat sorted.txt

acpi
adduser.conf
alternatives
anacrontab
apache2
apg.conf
.....
.....
etc

grep,egrep,fgrep:

fgrep matches patterns in a file. It doesn’t support regex. Instead it uses direct string matching.

egrep works in a similar way, but uses extended regular expression to match patterns.

grep is a combination of both.If you do not specify either -E or -F, (or their long form equivalents, --extended-regexp or --fixed-strings), grep behaves like egrep, but matches basic regular expressions instead of extended ones.

grep stands for  "Global Regular Expressions Print". The grep is a program that scans a file or group of files line by line and returns the output as the matched pattern. A pattern is an expression that specifies a set of strings which is meta characters.

the syntax for grep is

grep [OPTIONS] PATTERN [FILE...]

egrep

The acronym of egrep stands for  "Extended Global Regular Expressions Print".

egrep treats the given pattern as Regular expression

egrep is same as grep -E

fgrep

fgrep is same as grep -F  
fgrep stands for Fixed-string Global Regular Expressions Print

In fgrep the search will complete faster because it only processes a simple string rather than a complex pattern.

pgrep

pgrep stands for "Process-ID Global Regular Expressions Print".
pgrep is handy when you want to know is the process id integer of a process.
for example if we want to a process id of a process in order to kill that process first we need to find the process id
 ps -aux | grep process name

here by using pgrep we can directly get the pid of a process

gerp Search a Pa tern from current directory.

egrep (grep -E in linux) is extended grep where additional regular expression metacharacters have been added like +, ?, | and ().

fgrep (grep -F in linux) is fixed or fast grep and behaves as grep but does not recognise any regular expression metacharacters as being special.



$ grep hello testfirst

$ cat testfirst | grep hello
hello
hello w
hello world
hello sir
friend hello

$ grep ^hello testfirst
hello
hello w
hello world
hello sir

$ grep [e] testfirst
hello
hello w
hello world
hello sir
friend hello
helraj

$ grep [w] testfirst
two
hello w
hello world
$ grep [hpow] testfirst
two
ioslfsf
hello
hello w
hello world
hello sir
friend hello
helraj

$ grep ^[hpow] testfirst
hello
hello w
hello world
hello sir
helraj

$ grep ^[a-f] testfirst
ffaffadff
aff
friend hello

$ egrep -i 'hello|world' testfirst
$ egrep '^hello|world' testfirst
$ egrep -i 'hello. *world' testfirst

$ egrep 'hello' testfirst

tee command is used for read for standard input and write for standard out put

$ tee
