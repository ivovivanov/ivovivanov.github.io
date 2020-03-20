# Това за записки на Н. Георгиев от курса по 
# GNU/Linux system and network administration - A. Velin
# Записките са правени в лекциите по слайдове, затова на места има само нахвърляни някакви точки, именца и т.н.
# Сиреч още много има за четене, което не е записано тук.
# Също така не претендирам, че съм записал точно всичко, така че не разчитайте на 100% на записките.
# Местата с въпросителни ???? значат, че не съм записал нещо от слайдовете най-вероятно.



    Unix -многозадачна потребителска ОС- 1969 :Започва като страничен проект след провала на Multix. Съзаден от Ken Thompsom, Denis Ritchie, Brain Kernighan. 1973 Unix е пренаписан на C.

    Трите основни правила (леми):

       1. Всичко в операционната система е фаил
       2. Създават се малки специализирани програмини(не големи)
       3. Всичко в конфигурацията е текстов фаил ползващ ASCII  (American Standard Code for Information Interchange - Американски стандартен код за обмяна на информация)


    Standart streams

        Тук намерих картинката от слаидовете:)

    Richard Stallman

        * GNU (GNU`s Not Unix)(1983) пример за рекурсия
        * FSF(Free Software Foundation)(1985)
        * GNU GPL(General Public License)
              o Guarantees that free software remains free
              o All software under the GPL make source available to the end user
              o Changes to a GPL`d software package must also be licensed under GPL
              o Source code from one GPL`d software package can be incorporated in to other GPL`d software
        * Alix / Hurd -  това не ми стана много ясно какво е точно само съм записал ,че е разработка на някакъв kernel

Ядрото (kernel) на GNU - Hurd подлежи на дълъг процес на разработка, за това се използва Linux за kernel на GNU.

    The Free Software Definitoin - идеята е че free се употребява в смисъл на Свободен, не на Безплатен 
    - тук триябва да е дефиницията , но :) липсва 

    Книгата която ни препоръчаха : Free as in Freedom: Richard Stallman`s Crusade for Free Software

    Linux Kernel

        * Linus Torvalds - създателя на Linux ядрото
        * Minix - Unix операционна систем използвана с учебна цел
        * Th Linux Kernel
              o re-implementation of the UNIX API`s
              o GPL license
        * GNU/Linux
        * GNU/Hurd
        * GNU/kFreeBSD

    Standards - видове стандарти

        * Posix (Portable Operating System Interface for Unix)
        * Single Unix Specification - SUS
        * Filesystem Hierarchy Standard - FHS
        * Linux Standards Base - LSB - включва FHS като я надгражда

    Видове дистрибуции ( по-известните)

        * Slackware linux - най-старата все още подържана дистрибуция Patrick Volkerding
        * Debian 
              o стреми се да подържа високо ниво на GPL
              o няма определена компания която да разработва дистрибуцията
              o силно автоматизиран софуер
        * Ubuntu - базирана на Debian GNU/Linux ( Ubuntu - humanity towards others)
        * mint - базирана на Ubuntu, още по user friendly
        * Suse Linux и openSuse - openSuse e отворена дистрибуция на Suse
        * Red Hat Enterprise Linux distributions  и Fedora - Fedora е отворената дистрибуция на Red Hat
        * centOS - взима кода на Red Hat Enterprise Linux distributions и го пуска под GPL
        * free BSD - това е Unix не е Linux


    Login - процес на достъп до OS

        * Serial Terminals - текстово базиран
        * Virtual Terminals - текстово базиран
        * Network login - текстово базиран
        * GUI login (Graphic User Interface)
        * UID - user ID
        * UID 0 - сервизен потребител (root) privilege user - root , UID0
        *

    Switching User

        * su - change ID user or become super user
        * su -, -l, --login - получаване нова login сесия
        * sudo - execute a command as another user (само за една команда) , може да се конфигурира чрез допълнителен фаил

    Login Session Info

        * User ID (UID)
        * Group ID (GID)
        * pts -  pseudo - terminal slave
        * tty (Teletypewriter) - пълния път до терминал/сериен порт ,който  се използва
        * id - shows the current ID 
        * whoami - извежда user name 

    System info

        * users - списък на логнати потребители
        * who - show who is logged on
        * w - show who is logged on
        * finger  - информация за потребител
        * uname - a : print all system information 
        * free - display amount of free and user memory in the system
        * hostname - 
        * ifconfig - config a network interface


    Help

        * comman  --help; -h
        * man [section]  name
        * info (GNU replacement for man)

    $MANPATH, whatis and apropos

        * man -f , (whatis) - display manual page description
        * man -k , (apropos)

    File management and manipulation

        * FHS
        * Linux Standards Base

    FHS - The Root (/) Filesystem - стандарт

        * /bin - essential user command binaries (минимален набор команди за базова работа с ОС)
        * /boot - ядро на ОС, boot lader
        * /dev - device файлове, през които ОС осигурява достъп до устройствата
        * /etc - Host-specific system configuration (конфигурационни файлове)
        * /lib - специални share libraries и kernel modules (fetures) системи
        * /media - за монтиране на файлове 
        * /mnt 
        * /opt  - optinal software
        * /sbin - system binaries ( най-важните системни файлове за администратора) има още /usr/sbin и /usr/local/sbin
        * /srv - за изграждане на дърво с файлове, които ще предлагат сървиси на други ОС
        * /tmp - за временно съхранение на файлове
        * /usr -  вторична иерархия; в /usr/local - използва се за да се инсталират някаква програма от администратора без да ползва вече инсталирана дистрибуция
        * /var - contains variable data file

    До тук са задължителни. Ако може някой да ни напише кое за какво беше ще е страхотно 

        * /home - user home directory
        * /lib<qual> - тук беше нещо за 32-bit или 64-bit ...?(ако имаме 64bit ОС може да имаме директория lib32)
        * /root - home directory for the root user

    а тези са optional directory

    Virtual Hierarchies

        * /proc - Contains process info directories and other tunables
        * /sys - Exposes kernel konject data structurs
        * /dev/pts - ?

    Navigating the Filesystem

        * cd, pwd : changing and displaying directori
        * Absolute vs relativ addressing
        * cd (without parameters)
        * cd ~username
        * cd ~ (user home directory)
        * cd - 
        *  . (текуща) and .. (по-горна директория)

    Determining disk usage

        * df - report disk usage per file system (1000 instead of 1024 if --si is not set )
        * du - report disk usage per a file and directory
	
--------------------------------------------------------------------------------------  15.10.2011	    
    File Ownership
	* chown - change the user (UID) ownership 
		- only root can change ownership to another user
		- can also be used to change group at the same time
	* chgrp - modify just the group (GID) ownership (-R - recursively)
	* touch <name> - creates an empty file with "name"
    
    Default Group Ownership
	- Newly created files will usually be given GID ownership based on the current active group of the persho who creates the file
	* newgrp <new_group> - log in to a new groupcd
		- newly created files will be owned by the new group
		- users can only change to their own groups
		- root user can change to any group
		- exit to switch back
	- ex:
		maistora@debian:~$ su - root
		Password: 
		root@debian:~# newgrp maistora
		root@debian:~# touch gosho
		root@debian:~# exit
		exit
		root@debian:~# ls -l
		total 0
		-rw-r--r-- 1 root maistora 0 Oct 15 14:19 gosho


   File and directory Permissions
	* ls -l List file permissions <for the first symbol in drwxr-xr-x (this is directory because the first )>
		- - - regular file
		- b - block special file 
		- c - character special file
		- d - directory
		- i - symbolic link
		- p - FIFO (named pipe)
		- s - Socket
	
	- Permission sets for: 
		- user - UID that owns the file (sometimes called owner)
		- group - GID that owns the file
		- everyone else (sometimes called "other")
	- Permissions can be represented in two ways
		- symbolic representations (e.g. rwxr-xr-x)
		- numeric representation (e.g. 0755)
	
	special flags
		s s t	| r w x | r w x | r w x |
	_________________________________________
		4 2 1	| 4 2 1 | 4 2 1 | 4 2 1 |
		
			r-x - 5 
			rwx - 7 
			rw- - 6
			r-- - 4
	
   unmask
	- Default permissions for newly created filesystem objects
		- files: 666
		- directorie: 777
	* umask 
		- defines what permissions to withhold from the default permissions
		- дефинира каква стойност ще се извади от стандартната стойност за да получим правата които искаме


    Changing file Permissions
	* chmod - Modify the permissions
		- -R - recursively modify permissions
		- supports both numeric and symbolic notation
		- special permissions
		- set UID (SUID) - A program is executed with the file owner`s permissions (rather than with the permissions of the user who executes it).
			- ex. : password change (only root can write in the file with the passwords but a user can change his pass too)
		- set GID (SGID)
		- sticky
	- Special permissions cause different behavior for files and directories
	- user , group , others, all
	- chmod u=wrx,g=r-x

	- read - the permission to see the file
	- execute - to meke this file current file
	- write - the permission to change objects in the file

	- set special user flag - if it is set, when some other user Pencho executes the file it changes the permissions to one that created the file
		and have permissions to execute it.
	<set user ID on execution>
	-rwsr-xr-x - the "s" is the set flag
	-rwSr-xr-x - if it is capital "S" = something is wrong

	* passwd - changes the password
	* which passwd - shows where the command is stored </usr/bin/passwd>

    SGID and Sticky Bit on Directories
	- SGID 
		- 
	- Sticky bit
		- Normally in a directory that is world writable, sers can delete each other`s files. Setting the sticky bit overrides this behavior.
		- If I create a file in a dir and somebody else also creates file in the same dir if the sticky bit is set I can delete only my files
			and the other guy can delete only his.

    User private group scheme
	- UPG provides a convenient way to share files working in a group project directory
	- UPG scheme implemented by: 
		- placing each uer in their own private group
		- setting the umask to 0002
		- setting the group ownership of the project directory to a commonly shared GID
		- setting the project directory SGID

    Directory and file manipulation
	* mkdir - creates directories
		- mkdir -p - make parent directories as needed
		- mkdir -m - set permission mode
	* rmdir - deletes empty directories
	* cp - copies files and directories
	* mv - moves or renames files and directories 
	* rm - remove (deletes) files and directories < rm -RF - ATTENTION!!! remove recursively forced>
	* touch - creates empty files or pudates mtime and atime on existing files

	- mtime - last modification time
	- atime - last time accessed
	- ctime - creation time

    Physical Unix File Structure
	- Block and inode based
		- blocks hold data
		- inodes hold metadata
			- permissions on the file
			- access, modification and creation times for the file
			- owner of the file
			- size in bytes of the file
			- blocks occupied by the file
			- link count (names of the file)
			- inode number
		- directories (are files that) hold filenames and inodes
	- Superblock contains filesystem parameters
		- How many inodes, etc...

    Filesystem link 
	- Created with * ln
		- ln [OPTION] ... TARGET LINK_NAME 
		<it is recomended to use absolute path>
	- Hard links - a directory entry that references the same inode as another directory entry
		- can`t span filesystems (no hard-links between diff filesystems because they have their own pools with inodes)
		- can`t create hard links to non-existent file
		- can`t reference directories
		- do not occupy storage space (i.e. blocks)
	- Symbolic links -a file that references another file via path and name (ln -s)
		- can reference directories
		- can span filesystems
		- can reference non-existent files
		- occupy space
	* ln -i

    File extnsions and content <NO SUCH THING>
	- The system looks in the header to understand the file type
	- File extensions have no special meaning to the kernel
		- file extensions are just part of the file name
		- the kernel only distinguishes between executable non-executable (data) files
		- some application may care about extensions or otherwise use them for user convenience features
			- apache,file managers like Midnight Commander, OpenOffice.org/KOffice
	- * file - reports the type of file by examining the file contents
	
    Displaying text files
	* cat - displays entire file(s) (better for text files)
	* more - displays file(s) one screen at a time
	* less - more sophisticated and configurable pager
	
	* head - displays first 10 (by default) lines of file
	* tail - displays last 10 (by default) lines of file
		- tail -f  - to watch a file be appended to <continuous file reading>
	* -n option  - 

	- pager - cut a text to pages (cat, more, less)

    Displaying binary files
	- Displaying raw binary data may corrupt the display terminal
		* reset - corrects terminal 
		- [Ctrl-J] reset [Ctrl-J] (if carriage-return fails)
			- Why J? - Because in ASCII J = ENTER 
	* strings - displays ASCII text inside binary files <in binutils - apt-get install binutils> dpkg -S `which strings`
	* xxd - displays HEX and ASCII dump of file
	* clear - clear the terminal screen

    Searching the filesystem
	* find - searches a directory structure
		- First argument(s) are path(s) to start search from;
		- Next arguments specify criteria to search on: file name, size, permissions, type, owner, group, atime, mtime, ctime
		Last argumet specifies action to perform.
			- *-print - is the default action and displays matches
			- *-ls - displays full detail on matches
			- *-exec - allows a command to be run against each matching file. The -ok can be used when confirmation prompt is desired.
	* lookat - searches in DB which updates every 24 hours. Saves only filenames!!!

    Alternate Search Method 
	* locate - High-speed and low- ????
	???????

    Manually Installed Shared Libraries
	- Check for library dependencies with the "ldd" commnad
	* ld-linux.so - locates libraries to link to
		- /etc/ld.so.conf
		- /etc/ld.so.conf.d/
		- /etc/ld.so.cache
	- Run ldconfig command after installation of new libraries

    Archives with "tar" <tape archivator>
	* tar 
		- manipulates .tar files, also called tarballs
		- used for backup and transfer of files
		- creates, extracts or lists the contents of tarballs 
			* c, x, t, f, v <cvf> or <cvfz>
				- c - create
				- v - verbose 
				- f - file <uses "file" not a "tape" (лента)>
				
			- always use "f" option to 
		- GNU tar supports three built-in compression methods
	- .tar (tarball)
		- records file and directory structure
		- includes metadata about the file: date, timestamps, ownership, permissions, etc.
	- Comparession options
		- compress, gzip, bzip2, lzma

    Archives with cpio (трябва му списък от файловете)
	- manipulates .cpio files
	- used as the basis for RPM packages
	- doesn`t recurse sub-directories, must be passed list of directories
	- more rebust that tar when media errors encountered 
	- -i - input mode, used when feeding a cpio archive into the cpio command <input> (разархивиране)
	- -o - output mode, used to create cpio archives, which are sent to STDOUT <output> (архивиране)

    The gzip compression Utillity 
	* gzip - popular replacement for compress 
		- created by the GNU project beacause of patented algorithms in compress
		- default action deletes original after creating new compressed file
		- standard file extension: .gz
		- much higher compression ration than compress
	* gunzip or zcat decompresses files compressed with gzip
		- gunzip - decompresses the file on disk (removing the original, compressed file); 
		- zcat - outputs uncompressed data to STDOUT
    
    The bzip2 Compression Utility
	* bzip2 typically better compression than the gzip command 
		- typically better compression ????
		- ?????????????????????????????????

    The PKZIP Archiving / Compression format
	* zip - Compatible with PKZIP files
		- default action does NOT delete original file(s) after creating new compressed archive
		- standard file extension: .zip
	* unzip - expands a .zip file


--------------------------------------------------------------------------  22.10.2011

    Text processing and command line <fundamentals.03>
	* cat - Contatenate files
	* paste - marges text from multiple files - взема съдържанието на изредените файлове и ги слага на едно разделени с TAB
		- -s - merge files serially
		- uses tabs as default delimiter 

    File Statistics 
	- wc - print line , word, ad byte counts for each file
		* -c, --bytes - print the byte counts
		* -m, --chars - print the character counts
		* -l, --lines - print the newline counts
		* -w, --words - print the word counts

	- ex: 
		maistora@maistora:~$ wc -l /etc/passwd
		30 /etc/passwd

    Extracting Columns of Text
	* cut - Extracts selected fields from a line of text
		- can specify which fields you want to extract
		- uses tabs as default delimiter
		* -d - specify a different delimiter 
		- most useful on structured input (text with columns)

    	- ex 1: 5-12 <показва от 5-тия до 12-тия символ на всеки ред във файла>

		maistora@maistora:~$ cut -c 5-12 /etc/passwd
		:x:0:0:r
		on:x:1:1
		x:2:2:bi
		x:3:3:sy
		...
	- ex 2: < указваме delimiter ':' чрез -d ':' и чрез -f 1 <filename> указваме да ни изкара до 1вия delimiter на всеки ред във файл „filename“>

		maistora@maistora:~$ cut -d ':' -f 1 /etc/passwd 
		root
		daemon
		bin
		sys
		...

    	- ex 3: <Изкарваме 1-ва, 3-та и 5-та колона от /etc/passwd с делимитър ':'>

		maistora@maistora:~$ cut -d ':' -f 1,3,5 /etc/passwd
		root:0:root
		daemon:1:daemon
		bin:2:bin
		sys:3:sys
		sync:4:sync
		games:5:games

    Searching inside Files
	* grep - searches for patterns within files
		- -n - shows line numbers
		- -A NUM - prints match and NUM lines after match
		- -B NUM - prints match and preceding NUM lines
		- -C NUM - prints match and NUM lines before and after
		- -i - preforms case insensitive match
		- -v - inverts match; prints what doesn`t match
		- --color - highlight matched string in color

	- ex: 
		maistora@maistora:~$ grep -i --color SYSTEM /etc/passwd 
		gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/bin/sh
		hplip:x:109:7:HPLIP system user,,,:/var/run/hplip:/bin/false

	- ex: < търсим повече от един pattern >
		maistora@maistora:~$ grep -e false -e bash --color /etc/passwd
		root:x:0:0:root:/root:/bin/bash
		messagebus:x:101:103::/var/run/dbus:/bin/false
		Debian-exim:x:102:104::/var/spool/exim4:/bin/false


    The streaming editor
	* sed - stream editor for filtering and transforming text
	- usually the output of another program
	- ofter used to automate edits on many files quickly 
	- small and very efficient
	* -i - option for in place edits with modern versions


    Text processing with awk
	* awk - pattern scanning and processing language 
	- turning complete programming languate
	- splits lines into fields (like cut)
	- regex pattern matching (like grep)
	- math operations, control statemets, variables, IO...

	- ex: (показва първия и втория стринг от командата)
		maistora@maistora:~$ ps -ef | awk '{print $1,$2}'
		UID PID
		root 1
		root 2
		root 3
		...

    File redirection
	- file or I/O redirection allows you to redirect STDIN, STDOUT, and STDERR to files
	- Requeres special notation on the command line
		- redirect standard input with <
		* $ sort < /etc/passwd

		- redirect standard output with > 
		* $ echo 10000 > /proc/sys/fs/file-max - don`t do this

		- redirect standard error with 2>
		* $ ls - a1R /proc/ 2> /dev/null

		- redirect both STDOUT and STDERR to the same file: 
		* $ ls -R /proc/ > output 2>&1
		* $ ls -R /proc/ &> output

 	- /dev/null - черна дупка. каквото и да запишем всичко изчезва :D
	- /dev/zero - можем само да четем без нищо да прочитаме ?!?!
	- /dev/urandom - матрицата. връща безкрайна информация до безкрай

	- ex: <от командата "ls -a1R /proc/" всички грешки се записват в errlist и на изхода излизат само данни които не хвърлят грешка> 
		maistora@maistora:~$ ls -a1R /proc/ 2> /home/maistora/Desktop/errlist
   
    File redirection
	- < - redirects STDIN from a file
	- > - redirects STDOUT to a file (overwrite)
	- >> - redirects STDOUT to a file (append)
	- 2> - redirects STDERR to a file (overwrite)
	- 2>> - redirects STDERR to a file (append)
	- &> redirets both STDOUT and STDERR


    Text sorting
	* sort - sorts text
		- can sort on different columns 
		- by default sorts in lexicographical order < 1, 2, 234, 256, 29, 3, 4, 5>
		- can te told to sort numerically (by using the -n option) <1,2,3,4,5,29,234,256>
		- can merge and sort multiple files simultaneously
		- can sort in reverse order
		- often used to prepare input for the "uniq" command

 
    Piping Commands together
	- piping allows the STDOUT from one program (on the left of the pipe) to becom the STDIN of another (on the right of the pipe) ("The Unix way")
	* ls -al | less
	* cut -d: -f6 /etc/passwd | sort |uniq -c |sort -rn 
	- Redirection and piping can be combined:
		- usually used for feeding STDERR into the pipeling along with STDOUT
		* ls /proc/ 2>&1 | grep kernel
	
	- ex: (	изкарваме колоните от командата за процеси "ps -ef" от 3-та до 5-та колона като слагаме делимитър ' ' и изкарваме последните 10 реда
		чрез 'tail' и изкарваме HEX кода на резултата )

		maistora@maistora:~$ ps -ef | cut -d ' ' -f 3-5 | tail | xxd
		0000000: 3335 3138 2020 3335 3038 0a33 3635 3620  3518  3508.3656 
		0000010: 2032 3432 360a 3336 3737 2020 3234 3236   2426.3677  2426
		0000020: 0a33 3638 3520 2032 3432 360a 3336 3937  .3685  2426.3697
		... < 7 more rows >


   Replacing text characters
	* tr - translates, squeezes & deletes characters
	- translates one set of characters into another 
		- commonly used to convert lower case in to upper case
		* tr a-z A-z 

	- squeeze collapses duplicate characters 
		- commonly used to merge multiple blank lines into one 
		* tr -s '\n'

	- deletes a set of characters 
		- commonly used to delete special characters 
		* tr -d '\000'
	- ex: 
		maistora@maistora:~$ ps -ef | tail -1 | tr -s ' ' |  cut -d ' ' -f 1-3
		maistora 3800 2426

    Duplicate removal utility
	* uniq - removes duplicate adjacent lines from sorted text
	- cleanly combines lists of overlapping but not identical information
	* -c - refifixes each line of output with a number indicating number of occurrences
	- taking this output and performing a reverse ort produces a sorted list based on number of occurrences

	- ex: (	от passwd извеждаме 7ма колона, като сортираме за да извадим броя на последователните повтарящи се редове
		и след това ги сортираме по число чрез sort -n)

		maistora@maistora:~$ cat /etc/passwd | cut -d ':' -f 7 |sort| uniq -c | sort -n
		      1 /bin/sync
		      2 /bin/bash
		     10 /bin/false
		     17 /bin/sh

    Filename Matching 
	- many commands take a list 

    File globbing and wildcard patterns 
	- a wildcard pattern is a string that contains one of the characters: 
		- ? - matches any single character 
		- * - matches anything (any number of characters)
		- [...] - character classes - първия знак попадащ в множеството примерно [abcd]
			- the - character denotes a range
			- ex: [abcd2345] [a-d2-5] [a-gA-Z0-5]
			- ex: maistora@maistora:~$ ls -l /bin [bd] ash
			- ex: maistora@maistora:~$ ls -l /bin/*ash ash
			

    Brace Expansion 
	- allows generation of arbitrary strings
	- similar to wildcards, but target files or directories don`t need to exist
	- can have optional preamble and/or postamble
		- {m,n,o.on} expands to: m , n , o and on
		- d{m,n,o,on}t  ????????????
		????????????????????????????
	- ex: 
		maistora@maistora:/tmp$ touch a{1,2}b
		maistora@maistora:/tmp$ ls -l
		total 28
		-rw-r--r-- 1 maistora   maistora      0 Oct 22 16:50 a1b
		-rw-r--r-- 1 maistora   maistora      0 Oct 22 16:50 a2b

    General Quoting rules
	- metacharacters: \ ? ( ) $ ... * % { } [ ] - escaped with \ <backslash>
	- Backslash: \
	- Double Quotes: " " - if environmet var is taken with "var" it takes the actual value of the "var"
	- Single Quotes: ' ' - this escapes everything in it

    Nesting commnads
	- command substitution 
		- substitutes output of command in place of "embedded" command
	- nesting commnads
		- `command`
		- $(command)
	- Evluating commnad output
		- eval command
	- ex: 
		maistora@maistora:/tmp$ grep `cat /etc/passwd | cut -d ':' -f 7 |sort| uniq -c | sort -n | tail -1 | cut -d ' ' -f 7` /etc/passwd
		daemon:x:1:1:daemon:/usr/sbin:/bin/sh
		bin:x:2:2:bin:/bin:/bin/sh
		sys:x:3:3:sys:/dev:/bin/sh
		games:x:5:60:games:/usr/games:/bin/sh
		man:x:6:12:man:/var/cache/man:/bin/sh
		....



    Some usefull commands in command line: 
	Ctrl+A - go to the begining of the line
	Ctrl+E - go to the end of the line

--------------------------------------------------------------------------------------------------- 29.10.2011
 
    Evaluating Command Output
	$ ssh-agent
		SSH_AUTH_SOCK=/tmp.ssh-aqktrvn22891/agent.22891
			export SSH_AUTH_SOCK
		SSH_AGENT_PID=22892; export SSH_AGENT_PID;
		echo Agent pid 22892;
	
	$ eval $(ssh-agent)
	Agent pid 22897
	
	$ echo $SSH_AGENT_PID
	22897
	

    Multiple and Multi-line Commnads
	- Entering multiple commmands on one commnand line 
		- separate commnads with a semi-color ;
	- Entering multi-line commnads
		- Special use of the backslash (\) to do line-wrapping
		- This is sometimes called line wrapping or continuation

	- ex: 
		maistora@maistora:~$ seq 1 10
		1
		2
		3
		4
		5
		6
		7
		8
		9
		10

		maistora@maistora:~$ for i in `seq 1 10`; do echo b$i; done
		b1
		b2
		b3
		b4
		b5
		b6
		b7
		b8
		b9
		b10
		
		maistora@maistora:~$ for i in `seq 1 10`; do \			<we press ENTER>
		> echo b$i; \							<we press ENTER>
		> done
		b1
		b2
		b3
		b4
		b5
		b6
		b7
		b8
		b9
		b10

	** HW ** Хайзенбег бъг - Бъг който се променя когато се опиташ да го изследваш.

    Regular expression
	- Regular expressions (REs) provide a mechanism to select specific strings from one or more lines of text
	- complex language
	- grep, sed, perl...
	- man 7 regex  = man regex(7)

    Regular Expressions 
	- most characters, letters and numbers match themselves
	- special characters are matchable
	- . matches any single character
	- specify where the match must occur with anchors

    Re Secial characters
	- \t - tab
	- \n - newline / line feed		- 10 ASCII (LF - line feed)
	- \r - carriage return		- 13 ASCII (CR - carriage return)
	- \f - form feed
	- \c - control characters
	- \x - character in hex
	- .  - any single character

    Кой е 10 и кой е 13 в ASCII?

    RE Anchors
	- ^RE - anchor RE at start of line
	- RE$ - anchor RE at end of line
	- \<RE - anchor RE at start of word
	- RE\> - anchor RE at end of word

    RE character classes
	- Character classes, [...], match any single character in the list
		- RE [0123456789] = [0-9] - matches any single digit
	- Some predefined character classes 
		- [:alnum:] [:alpha:] [cntrl:] [:digit:]
		- ?????????

    RE character classes
	- [:alnum:] letters and digits
	- [:alpha:] letters
	- [:cntrl:] control characters
	- [:digit:] digits
	- [:graph:] printable characters (w/o space)
	- [:lower:] lower case letters
	- [:upper:] lower case letters
	- [:print:] printable characters
	- ??????

    RE Character Class examples
	* grep [[:upper:]] /etc/passwd
		- ex:
			maistora@maistora:~$ grep [[:upper:]] /etc/passwd --color
			list:x:38:38:Mailing List Manager:/var/list:/bin/sh
			gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/bin/sh
			Debian-exim:x:102:104::/var/spool/exim4:/bin/false
			avahi-autoipd:x:104:107:Avahi autoip daemon,,,:/var/lib/avahi-autoipd:/bin/false
			avahi:x:105:108:Avahi mDNS daemon,,,:/var/run/avahi-daemon:/bin/false
			Debian-gdm:x:107:115:Gnome Display Manager:/var/lib/gdm3:/bin/false
			hplip:x:109:7:HPLIP system user,,,:/var/run/hplip:/bin/false
			haldaemon:x:110:118:Hardware abstraction layer,,,:/var/run/hald:/bin/false

	* egrep '^[rb]' /etc/passwd - началото на реда ще започва или с r или с b
		- ex:
			maistora@maistora:~$ grep '^[rb]' /etc/passwd --color
			root:x:0:0:root:/root:/bin/bash
			bin:x:2:2:bin:/bin:/bin/sh
			backup:x:34:34:backup:/var/backups:/bin/sh

		- ex: - всички които започват с r или b и за втори символ имат o или i
			maistora@maistora:~$ egrep '^[rb][oi]' /etc/passwd --color
			root:x:0:0:root:/root:/bin/bash
			bin:x:2:2:bin:/bin:/bin/sh

		- ex: -
			maistora@maistora:~$ egrep '^.[oi]' /etc/passwd --color
			root:x:0:0:root:/root:/bin/bash
			bin:x:2:2:bin:/bin:/bin/sh
			list:x:38:38:Mailing List Manager:/var/list:/bin/sh
			nobody:x:65534:65534:nobody:/nonexistent:/bin/sh
			libuuid:x:100:101::/var/lib/libuuid:/bin/sh

	* egrep '^[^rb]' /etc/passwd - всички които не започват с r или b
		- ex: - 
			maistora@maistora:~$ egrep '^[^rb]' --color /etc/passwd
			daemon:x:1:1:daemon:/usr/sbin:/bin/sh
			sys:x:3:3:sys:/dev:/bin/sh
			sync:x:4:65534:sync:/bin:/bin/sync
			games:x:5:60:games:/usr/games:/bin/sh
			man:x:6:12:man:/var/cache/man:/bin/sh
			lp:x:7:7:lp:/var/spool/lpd:/bin/sh
			mail:x:8:8:mail:/var/mail:/bin/sh
			news:x:9:9:news:/var/spool/news:/bin/sh
			uucp:x:10:10:uucp:/var/spool/uucp:/bin/sh
			proxy:x:13:13:proxy:/bin:/bin/sh
			www-data:x:33:33:www-data:/var/www:/bin/sh
			list:x:38:38:Mailing List Manager:/var/list:/bin/sh
			irc:x:39:39:ircd:/var/run/ircd:/bin/sh
			gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/bin/sh
			nobody:x:65534:65534:nobody:/nonexistent:/bin/sh
			libuuid:x:100:101::/var/lib/libuuid:/bin/sh
			messagebus:x:101:103::/var/run/dbus:/bin/false
			Debian-exim:x:102:104::/var/spool/exim4:/bin/false
			statd:x:103:65534::/var/lib/nfs:/bin/false
			avahi-autoipd:x:104:107:Avahi autoip daemon,,,:/var/lib/avahi-autoipd:/bin/false
			avahi:x:105:108:Avahi mDNS daemon,,,:/var/run/avahi-daemon:/bin/false
			usbmux:x:106:46:usbmux daemon,,,:/home/usbmux:/bin/false
			Debian-gdm:x:107:115:Gnome Display Manager:/var/lib/gdm3:/bin/false
			saned:x:108:117::/home/saned:/bin/false
			hplip:x:109:7:HPLIP system user,,,:/var/run/hplip:/bin/false
			maistora:x:1000:1000:maistora,,,:/home/maistora:/bin/bash
			haldaemon:x:110:118:Hardware abstraction layer,,,:/var/run/hald:/bin/false


    RE Quantifiers
	- Control the number of times a preceding RE is allowed to match
		- * - match 0 or more times
		- + - match 1 or more times
		- ? - match 0 or 1 times
		- {n} - match exactly n times
		- {n,} - match at least n times
		- {n,m} - match between n and m times

    RE Quantifiers
	$ egrep '^[stu].{14}$' /usr/share/dict/words 		- starts with s or t or u, then 14 random symbols and end of line
	$ egrep '^[auiou].{9}ion$' /usr/share/dict/words 	- starts with a or u or i or o or u then 9 randoms and ends with ion and end of line
	$ egrep '^c.{15,}$' /usr/share/dict/words 		- starts with c then at least 15 randoms and end of line
	$ egrep '^n.{6,10}c$' /usr/share/dict/words		- starts with n then from 6 to 10 randoms and then c and end of line

    RE parenthesis
	- (RE) - creating a new atom
	- (RE)\non-zero digit storing values
	- (RE1 | RE2) - alternation: RE1 or RE2
	- abc{3} vs. (abc){3}
		- abc{3} = abccc
		- (abc){3} = abcabcabc	

	$ cat file
	- Parenthesis allow you to store matched patterns.
	$ sed -r 's/(.)\1/\[\1\1]/g' file            		- между първите /../ какво ще мачваме а между вторите с какво ще замениме. 
								- ТОВА ПРОМЕНЯ САМО ИЗХОДА, не променя самия файл.
								- като намери 2 еднакви букви една до др ги загради в квадратни скобки
		- /g - global
		- s  - ???
	Parenthesis a[11]ow you to store matched pa[tt]rns.
	* egrep '(dog|cat)' file


	- ex: 
		maistora@maistora:~/Desktop$ egrep '([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])\.([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])\.([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])\.([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])' ifconfig.log --color
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet addr:10.2.4.6  Bcast:10.2.255.255  Mask:255.255.0.0

	- better ex: 
		egrep '([1-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])\.(([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])\.){2}([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])' ifconfig.log --color


    Text Editing
	- Unix Revolves around text
		- text is rebust
		- text is universally understood
		- the only tool / program required is a text editor
		- remote administration possible over lol-bandwidth connections
	- Text editors
		- many editors available, each with fanatical followings
		- Pico/Nano, vi and Emacs are the most common
		- $EDITOR control default editor

    vi / vim
	- vi - The visual Editor
		- developed originally by Bill Joy for BSD UNIX
		- Officially included in AT ?????????
		?????????????????

    vi help
	- Books & Cheat Sheets
	- :help - Vim has extensive online help
	- http:// ????

    Basic vi commands
	- Modes 
		- Insert Mode: keystrokes are interested into the document 
		- Cammand Mode: keystrokes are interpreted as commands
	- Basic Cursor Movement Commands
		- hjkl
	- Basic Editing Commands
		- i a [ESC] x dd
	- Saving & Exiting 
		- :w
		- :q
		- :wq
		- :wq!

-------------------------------------------------------------------------------------------------------------------------------------- 5.11.2011
	Process 
		- A process is a launched program
			- application
			- process
			- thread
		- Associated with a process:
			- precess ID (PID)
			- priority
			- nice value
			- memory
			- security context
			- environment
			- file handles

	
	Process Creation
		- Processes are organized in a hierarchy
			- init 
				- first process spawned by kernel with PID of 1
				- the only process directly launched by the kernel
				- init will spawn child processes
			- child processes spawn other children which can spawn other children, etc...
		- Processes can be created by two methods
			- fork() - create duplicate of self (as a child process)
			- exec() - spawn completely new process

	Process States
		- Processes can trasition between states upon recipt of signals
			- RUNNING - currently running 
			- INTERRUPTABLE - sleeping but can be woken up
			- UNINTERRUPTABLE - sleeping but can not be woken up
			- ZOMBIE - terminated but its status was not collected
			- STOPPED - stopped by a debugger or job control

	Process state condes 
		- D - uninterruptible sleep (usually IO)
		- R - running or runnable (on run queue)
		- S - interruptible sleep (waiting for an event to complete)
		- T - stopped, either by a job control signal or because it is being traced
		- W - paging (not valid since the 2.6.xxx kernel)
		- X - dead (should never be seen)
		- Z - defunct ("zombie") process, terminated but not reaped by its parent

	Viewing Processes
		* ps - standard process listing tool
			- User /proc/ as information source
			- Can customize displayed output
			- Supports BSD (aux) and SysV options (eaf)

		* pgrep - ps and * grep combined

		* pstree
			- Shows process tree

		* top / htop 
			- Provides summary information and stats on each running process in real-time fashion
		
		* jobs 
			- Displays backgrounded/suspended processes invoked from shell 

		ex: show all processes with ps
			maistora@maistora:~$ ps -aef

		ex: using top - very cool, see man 
			maistora@maistora:~$ top 

		ex: ps -ef
			- columns: 
				- UID 	- user ID - owner
				- PID 	- process ID 
				- PPID 	- parent process ID 
				- C 		- cpu utilization (не е сигурно че е това)
				- STIME	- 
				- TTY	- 
				- TIME 	- 
				- CMD 	- 

****** HW - с какво се занимава kthreadd (от *ps -ef втория процес)
	- ans:	-  kthreadd() is main function (and main loop) of daemon kthreadd which is a kernel thread daemon, the parent of all other kernel threads.

****** HW - как изглежда ASCII таблицата (pstree и pstree | less - разлика на output-a)
	- ans:	- като се извика pstree | less -  less форматира текста така че да е удобнен за която и да е команда в следващия pipe
		
****** HW:
		ex: от top командата load average 5/10/15 min   	- въпрос за работа в GOOGLE
	-ans: http://www.linuxjournal.com/article/9001
		- 
		Самият той е доста гадна величина...

		Точното значение е "в последните 5, 10, 15 минути през цялото време
		колко процеси са били runnable, т.е. било е възможно да работят". Това
		включва процеси, чакащи за I/O и процеси, чакащи за процесорно време.

		От това има няколко нетривиални последици, които лесно може да видите
		тестово. Ако си монтирате произволна мрежова файлова система (nfs, smb,
		cifs), започнете да работите с нея и си откачите мрежата, то всеки
		процес, който ги ползва в момента, ще качи с 1 loadavg. Нещо подобно
		може да се получи с откачени/умрели/бавни дискове.

		В повечето случаи loadavg помага за начален поглед в/у машината, т.е.
		"има ли нещо нередно", но рядко може да е полезен за нещо повече.
		(също така, поне по последни мои спомени в повечето случаи като стигне
		1024 и се превърта, но това много рядко може да се види)

	*top:
	Cpu(s): 
		us - users cpu usage
		sy - system
		ni - nice
		id - ....

	Signals 
		- Special message that can be sent to a process
		- Processes can install signal handlers that catch signals and trigger some action
		- Signals can have different meanings on different architectures
		- Some signals cannot be caught or ignored and are processed by the kernel (SIGKILL (9))



	Signal - man page
		- signal (7)
		* SIGHUB (1) - terminate 	- Hangup detected on controlling terminal or death of controlling process
		* SIGINT (2) - terminate 		- Interrupt from keyboard	(Ctrl-C)
		* SIGQUIT (3) - terminate & dump core 	- Quit from keyboard
		* SIGKILL (9) - terminate		- Kill signal
		* SIGSEGV (11) - terminate & dump core - Invalid memory reference
		* SIGTERM (15) - terminate	- Termination signal
		* SIGSTOP (19) - stop		- Stop process	(Ctrl-Z)

	
	How to send signals 
		* kill - send arbitrary signals to process by PID 
			- sends a SIGTERM (15) by default
			- -l - lists all signlas supported on the machine
		* killall - send signal to process by name
		* pkill - send signal to process by terminal, group, username, PID, or command name
		- From keyboard
			- Ctrl-c = SIGINT (2)
			- Ctrl-z = SIGSTOP (19)


	Process Scheduling 
		- nice value [-20, 19] - колко този процес ще бъде най-очтив към другите процеси. Колкото по-голямо е числото толкова по-малко ресурси взема процеса 
							и е по-добър за другите процеси. 
						- потребителя може да променя своя процес, но само като увеличава числото, не може да го намалява (не може да става по-нахален).
		-Launch a process with an adjusted scheduling priority:
			* nice <name>
			* nice -n 15 <name>
			* nice -n -10 <name>

		- Modify the scheduling priority of a running process: 
			* renice 10 <pid>
			* renice -10 <pid>
			* renice 0 -p <pid>
			

	Job control
		- job control refers to the ability to selectively stop (suspend) the execution of processes and continue (resume) their execution at a later point.
		- The Linux kernel supports job control functions
		- These functions are exposed to the user via the shell (ex. bash)
		- Job control .. ????

	Jobs
		- Start a process as a background process by running * <program> &     	(ако има някакъв stdout той ще излиза на нашия екран. може да го редиректнем към файл)
		- Stop an already running process by sending it a SIGSTOP (19), (Ctrl-Z)
			- fg - run the job in the foreground
			- bg - run the job in the background
			- kill - terminate the job
		- Refer to jobs using %n where 'n' is the job number
			- %1 	=	fg 1
			- %1 &	=	bg 1

		- The jobs command will list all jobs present on the shell but can not list jobs for other shells 
		- Работи само за текущия shell

	ex: tail -f  (заради -f е да чете постоянно от файла и да обновява)
		maistora@maistora:~$ logger aasdf   			- makes entries in the system log.

		maistora@maistora:~$ tail -f /var/log/syslog 
		Nov  5 15:24:50 maistora avahi-daemon[1240]: Received response from host 10.255.3.21 with invalid source port 49627 on interface 'wlan0.0'
		Nov  5 15:24:51 maistora avahi-daemon[1240]: Received response from host 10.255.3.21 with invalid source port 49627 on interface 'wlan0.0'
		Nov  5 15:24:52 maistora avahi-daemon[1240]: Received response from host 10.255.3.21 with invalid source port 49627 on interface 'wlan0.0'
		Nov  5 15:24:53 maistora kernel: [ 7543.540040] eth0: auto-negotiating...
		Nov  5 15:24:53 maistora avahi-daemon[1240]: Received response from host 10.255.3.21 with invalid source port 49627 on interface 'wlan0.0'
		Nov  5 15:25:03 maistora kernel: [ 7553.564030] eth0: auto-negotiating...
		Nov  5 15:25:13 maistora kernel: [ 7563.588039] eth0: auto-negotiating...
		Nov  5 15:25:23 maistora kernel: [ 7573.612030] eth0: auto-negotiating...
		Nov  5 15:25:33 maistora kernel: [ 7583.636027] eth0: auto-negotiating...
		Nov  5 15:25:43 maistora kernel: [ 7593.660030] eth0: auto-negotiating...
		Nov  5 15:25:53 maistora kernel: [ 7603.684041] eth0: auto-negotiating...
		Nov  5 15:26:03 maistora kernel: [ 7613.708028] eth0: auto-negotiating...
		Nov  5 15:26:13 maistora kernel: [ 7623.732029] eth0: auto-negotiating...
		Nov  5 15:27:02 maistora maistora: aasdf									- ЕТО ТУКА Е

		// CTRL + Z
		^Z
		[1]+  Stopped                 tail -f /var/log/syslog
		maistora@maistora:~$ jobs
		[1]+  Stopped                 tail -f /var/log/syslog

		maistora@maistora:~$ jobs
		[1]+  Stopped                 tail -f /var/log/syslog
		maistora@maistora:~$ fg 1
		tail -f /var/log/syslog
		Nov  5 15:29:03 maistora kernel: [ 7794.140032] eth0: auto-negotiating...
		Nov  5 15:29:13 maistora kernel: [ 7804.164029] eth0: auto-negotiating...
		Nov  5 15:29:23 maistora kernel: [ 7814.188029] eth0: auto-negotiating...
		Nov  5 15:29:33 maistora kernel: [ 7824.212029] eth0: auto-negotiating...
		Nov  5 15:29:43 maistora kernel: [ 7834.236028] eth0: auto-negotiating...
		Nov  5 15:29:53 maistora kernel: [ 7844.260030] eth0: auto-negotiating...
		Nov  5 15:30:03 maistora kernel: [ 7854.284030] eth0: auto-negotiating...
		Nov  5 15:30:13 maistora kernel: [ 7864.308030] eth0: auto-negotiating...
		Nov  5 15:30:23 maistora kernel: [ 7874.332035] eth0: auto-negotiating...
		Nov  5 15:30:33 maistora kernel: [ 7884.356026] eth0: auto-negotiating...
		^Z
		[1]+  Stopped                 tail -f /var/log/syslog
		maistora@maistora:~$ jobs
		[1]+  Stopped                 tail -f /var/log/syslog
		maistora@maistora:~$ bg 1
		[1]+ tail -f /var/log/syslog &
		Nov  5 15:30:43 maistora kernel: [ 7894.380030] eth0: auto-negotiating...
		Nov  5 15:30:53 maistora kernel: [ 7904.404037] eth0: auto-negotiating...
		maistora@maistora:~$ Nov  5 15:31:04 maistora kernel: [ 7914.428029] eth0: auto-negotiating...
		Nov  5 15:31:14 maistora kernel: [ 7924.452056] eth0: auto-negotiating...
		Nov  5 15:31:24 maistora kernel: [ 7934.476034] eth0: auto-negotiating...
		Nov  5 15:31:34 maistora kernel: [ 7944.500028] eth0: auto-negotiating...
		Nov  5 15:31:44 maistora kernel: [ 7954.524040] eth0: auto-negotiating...



		Process
		------------
		T	- Stopped 
		S 	- Sleeping
		R	- Running (FG/BG)

		Ctrl-Z - Stopped
		Ctrl-C - Изпраща SIGINT и се надяваме програмиста да е написал handler за него и това да изключи програмата по нормалния път. Ако не е направил се извиква по default SIGINT(2) което terminate-ва приложението. Може да се извика SIGQUIT (3) което ще го terminate-не и ще го dump-не и няма да може да се дебъгне. А програмиста може да е написал handler за прихващане на тези 2 сигнала и да не прави нищо с тях. В този случай нищо няма да се получи от Ctrl-C. В този случай трябва да използваме нещо по-силно за да го изключим - kill. 
		

	1) dump-ването представлява копиране на паметта на процеса в един файл,
	т.нар. core dump (който най-често се казва core и се сипва в текущата
	директория). Той се използва за дебъгване на гръмнали приложения.

	2) Сигналите си имат default-но поведение, което е описано в signal(7).
	Всички без няколко специфични прекратяват работата на приложението, ако
	не са прихванати. Няколко от тях водят и до core dump (SIGSEGV, SIGBUS).

	3) Стандартният convention за ползване на сигнали изглежда горе-долу по
	следния начин:
	SIGINT, SIGTERM прекратяват приложението и по принцип могат да се
	прихванат, за да се направят някакви cleanup операции. Рядко се
	игнорират, но се случва cleanup-а да се забави.
	SIGKILL не може да се прихване от нищо (обработва се директно от ядрото
	и убива приложението)
	SIGSEGV, SIGBUS и компания се подават при опити за достъп на
	несъществуваща памет и по принцип не се препоръчва да се прихващат,
	освен ако не се използват за специфични (извратени) случаи, така че да
	се получи coredump и хората да могат да дебъгват на спокойствие.
	SIGHUP прекратява конзолните приложения (подобно на SIGINT), и се
	използва в демони и други процеси за чисто контролен сигнал (да им се
	каже да си презаредят конфигурационните файлове например). (някъде
	по-горе беше объркан със sighub, по принцип идва от hang-up, като
	затваряне на телефонната слушалка)



	Command shell
		- user-interface
		- access to filesystem
		- scriptability for task automation
		- program launchinng
		- process control interface

	Shells 
		- Thompson Shell (sh) - Ken Thompson, 1971, AT&T
		- Bourne Shell (sh) - Stephen Bourne, 1977, AT&T - Всички след него гледат на него като стандарт
		- C Shell (csh) - Bill Joy, 1978, BSD
		- Korn Shell (ksh) - David Korn, 1983, AT&T
		- Enhanced C Shell (tcsh) - Ken Geer, 1975-1983, CMU
		- Bourne Again Shell (bash) - Brian Fox, 1989, GNU
		- Z Shell (zsh) - Paul Falstad, 1990, Princeton - По-лек и прост от bash
		- Debian Almquist Shell (dash) - port of NetBSD ash to Linux by Herbert Xu 1997, renamed dash 2002

	which shell?
		- Login shell name stored in $SHELL environment variable
		- Identifying the login shell: 
			* echo $SHELL
		- Identifying the current shell: 
			* ps -f

	Changing the shell
		- Use the shell name to invoke that shell (ex: * dash)
		- Changinng login shell permanently 
			- Edit the /etc/passwd entry for that user
			* chsh - (change shell) available to normal users
		- /etc/shells - contains list of allowed shells

	sh
		- Simple.
		- Prompt is set using the PS1 variable
			* PS1="$(hostname) $ "
		- контролираме какъв стринг ще се изписва пред курсора ни в конзолата. Командата горе ще направи 'maistora $'
		- . /file.sh		- променливите които се създават при изпълнението се премахват след него
		- . file.sh		- променливите които са създадени при изпълнението остават валидни в текущата сесия
		
****** HW - за какво се използват:
		- PS2, PS3, PS4  
	-ans: http://www.thegeekstuff.com/2008/09/bash-shell-take-control-of-ps1-ps2-ps3-ps4-and-prompt_command/
		- PS = Prompt statement
		- PS1 - Default interaction prompt
		- PS2 - Continuation interactive prompt 
				- A very long unix command can be broken down to multiple line by giving \ at the end of the line. 
				The default interactive prompt for a multi-line command is “> “.  
				We can change this default behavior to display “continue->” by using PS2 environment variable.

		- PS3 - Prompt used by “select” inside shell script
				- You can define a custom prompt for the select loop inside a shell script, using the PS3 environment variable.

		- PS4 - Used by “set -x” to prefix tracing output
				- The PS4 shell variable defines the prompt that gets displayed, when you execute a shell script in debug mode as shown below.

 	
	bash 
		- Completely backwards compatible with Bourne shell
		- Adds several enhancement - many from csh / tcsh.
			- commnad-line history and completion
			- aliases 
				ex: 	maistora@maistora:~$ alias ll='ls -la'
					maistora@maistora:~$ alias
						alias ll='ls -la'
						alias ls='ls --color=auto'

			- sophisticated prompt configuration
			- both Emacs and vi style command line editing
			- tilde (~ ) as an alias for home directories
			- Ctrl-x , Ctrl-v - едно след друго се избират.
				maistora@maistora:~$ 
				GNU bash, version 4.1.5(1)-release (i486-pc-linux-gnu)


	bash: Commad Editing
		- bash shell offers vi-mode and Emacs-mode command editing
			* set -o vi 		- преминаване във vi режим (в insert режим на vi)
			* set -o emacs


		maistora@maistora:~$ echo $PS1
		\[\e]0;\u@\h: \w\a\]${debian_chroot:+($debian_chroot)}\u@\h:\w\$
		maistora@maistora:~$ unset PS1
		PS1="$"
		$PS1="\u@\h \! $ "

		- Докато не променим конфигурационните файлове няма да има трайна щета. 
		- файловете са .bashrc и .bash_profile


****** HW Какви клавишни комбинации подържа bash?
	
	Ctrl + A	- Go to the beginning of the line you are currently typing on
	Ctrl + E	- Go to the end of the line you are currently typing on
	Ctrl + L    - Clears the Screen, similar to the clear command
	Ctrl + U	- Clears the line before the cursor position. If you are at the end of the line, clears the entire line.
	Ctrl + H	- Same as backspace
	Ctrl + R	- Let’s you search through previously used commands
	Ctrl + C	- Kill whatever you are running
	Ctrl + D	- Exit the current shell, deletes chars under the cursor
	Ctrl + Z	- Puts whatever you are running into a suspended background process. fg restores it.
	Ctrl + W	- Delete the word before the cursor
	Ctrl + K	- Clear the line after the cursor
	Ctrl + T	- Swap the last two characters before the cursor
	Esc + T	- Swap the last two words before the cursor
	Alt + F	- Move cursor forward one word on the current line
	Alt + B	- Move cursor backward one word on the current line
	Tab		- Auto-complete files and folder names



 	bash: Command Completion
		- Procedure depends on editing mode in use
			- [TAB] for simple completion in emacs mode
			- \ - (from control mode) for simple completion in vi mode
		-More advanced completion than csh or ksh
			- support: command, file / directory name, username(~), hostname(@), and variable($) name completion
			- attempts to "do the right thing" based on context
			- highly customizable (~/.inputrc)
				* set completion-ignore-case
				* set completion-query-items
				* set print-completion-horizontally
				* set show-all-if-ambiguous

	
	Shell and Environment Variables
		- Useful in shell scripting
			- /etc/profile,  .profile,  .bash_profile,  .bashrc
		- Programs may malfunction if not set ($PATH, $HOME, $USER, etc.)
		- Viewing variables 
			* set (shell) 			- валидни за текущата сесия
			* env (environment)		- валидни за текущата сесия + наследявани за child процесите
		- Clearing variables
			* unset (shell | environment)	- за премахване на променлива за shell или environment променливи
			* env -u|i <command> (environment)

		* export - прави от shell променлива във environment


	Shell and Environment Variables 
	$ FOO=42; echo $FOO
	$ bash
	$ echo $FOO
	$ exit
	$ echo $FOO
	$ unset FOO; echo $FOO



	Environment Variables 
		$PATH - executable search path
		$PWD - path to current working directory
		$TERM - Login terminal type (e.g. vt100, xterm)
		$SHELL - Path to login shell (e.g. /bin/sh)
		$HOME - Path to home directory (e.g. /home/foo)
		$USER - Username of user
		$DISPLAY - X display name (e.g. station2:0.0)
		$EDITOR - Name of default editor (e.g. ex)
		$VISUAL - Name of visual editor (e.g. vi)


	maistora@maistora:~$ export EDITOR=nano
	maistora@maistora:~$ crontab -e					- разчита на дефинирания от нас редактор да прочете съдържанието и да го редактира.
	no crontab for maistora - using an empty one
	No modification made
	maistora@maistora:~$ export EDITOR=pico
	maistora@maistora:~$ crontab -e
	no crontab for maistora - using an empty one
	No modification made
	maistora@maistora:~$ export EDITOR=vi
	maistora@maistora:~$ crontab -e



---------------------------------------------------------------------------------------------------------------- 12.11.2011

	. = source	
	./ - пали се в нов интерпретатор, когато приключи всички използвани ресурси и променливи се освобождават
	.  - пали се в текущия интерпретатор и всичко се пази след изпълнението на скрипта и може да се използва
	source  - пали се в текущия интерпретатор (също е като . )

	shell scripts parameters 
		- Command line arguments in $0, $1, $2, ...
			- $0 - is name of shell script (foo.sh)
			- $1 - is first argument, $2 is second, ...
		- Number of arguments in $#
		- List of all parameters in $0

		- for making a shell script file it have to start with #!/bin/bash

	????????????????????

	shell mathematics & comparison
		$ foo=$((12*34))
		$ echo $foo
		408
		$ echo $((56+$foo))
		464

		* expr(1)
		* perl(1), awk(1), bc(1)

		* test(1)

	exit status
		- $? - показва каква е exit стойността на скрипта който сме изпълнили
		- 0 - successful
		- 1-255 - faild

		- exit
		- exit 1
		- echo $?

	shell: conditions
		- test condition
		- test condition && true-command
		- test condition test condition || false-command
		- test condition && true-command || false-command

		test 5 -gt 2 && echo "Yes"
		test 1 -lt 2 && echo "Yes"
		test 5 -eq 15 && echo Yes || echo No
		test -f /etc/resolv.conf && echo "file /etc/resolv.conf found." || echo "file /etc/resolv.conf not found."


	shell: if
		- if 	then
		- if 	then 	fi
		- if 	then 	else 	fi
		- if 	then 	elif 	else	fi
		
		- fi - край на statement

		#!/bin/bash
		read -p "Enter number : " n
		if test $n -ge 0
		then 
			echo "$n is positive"
		else 
			echo "$n is negative"
		fi

****** HW - същата задача но по гъзарска

	shell: case

	case $var-name in 
		pattern1)
			command1
			... 
			commandN
			;;
		pattern2)
			command1
			...
			commandM
		*) 				- за всички останали
			command1
			...
			commandZ
	esac



	shell: for loop
		
		for VARIABLE IN 1 2 3 4 .. N 
		do
			command1 
			command2
		done

		for i in 1 2 3 4 5; do echo "i is $i"; done
		for i in {0..10..2} ; do echo $i ; done			- от 0 до 10 със стъпка 2

		ex: 
			maistora@maistora:~/Desktop$ for i in {0..10..2} ; do echo $i ; done
			0
			2
			4
			6
			8
			10

			maistora@maistora:~/Desktop$ for i in {a..z} ; do echo $i ; done
			a
			b
			..
			z

	shell: for loop
	
		for (( EXP1; EXP2; EXP3))
		do 
			command1
			command2
		done

		for ((c=1; c<=5; c++)); do echo $c ; done
		for (( ; ; )) ; do echo "foo"; done			
	
	shell: for loop
		

	shell: while loop

		while [condition]
			do 
				command1 
				command2 
				...
				commandN
			done

		#!/bin/bash
		n=1
		
		while [ $n -le 5 ]
		do 
			echo "n is $n"
			n=$(( n+1 ))
		done


	shell: functions 
		* declare -f 
		* unset -f <function-name>

		hello() { echo "function parameter is $1" ; }

		:(){ :|:& };:  		- fork bomb - Форк бомба - може да убие машината ако сме root !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! - възможно е да забие машината.
		
		bomb() {
			bomb | bomb &		
		}; bomb

****** HW - Как да се предпазим от fork bomb? '(script_name)$'
then
	  - ans: /etc/security/limits.conf


	at
		?????

	cron 
		- executs jobs at a recurring interval
		- each user has a cron table which describes what to execute ant at what interval
		??????????

	crontab format
		- crontab(5)
		- minute	0-59
		- hour 	0-23
		- day of month 	1-31
		- month 	1-12
		- day of week 	0-7	- неделя е и 0 и 7 заради разликите тук и в американския стандарт
		- *
		- 1, 2, 5, 9
		- 0-4, 8-12
		- 0-23/2		- през 2 часа


		- няма начин да се направи на през 7 мин.
	contab ex
		5 0 * * * $HOME/bin/daily/.sh >> $HOME/tmp/out 2>&2	- всеки месец всеки ден в 0 часа и 5 минути
		15 14 1 * * $HOME/bin/monthly.sh			- всеки месец на първи в 14 часа и 15 минути

	/etc/cron*/	- Разгледай си файловете.
		* /etc/cron.d/
		* /etc/crontab
		* /etc/cron.hourly/
		* /etc/cron.daily/
		* /etc/cron.weekly/
		* /etc/cron.monthly/

****** HW: Какво е anacron?    man anacron(8) - независимо дали машината е включена се изпълнява 

Ex: To start

maistora@bt:~/stuff/Touchpad$ touch touch_off.sh
maistora@bt:~/stuff/Touchpad$ sudo chmod 755 touch_off.sh 
maistora@bt:~/stuff/Touchpad$ ./touch_off.sh 

	* chsh - променя текущия shell
	- bash_loing и bash_logout - изпълняват се при login и logout


---------------------------------------------------------------------------------------- 19.10.2011

      - В Unix света винаги има поща, била тя дори локална.

****** HW ---------------
   V сутрин в 1 и 30 пон, сряда и петък, да прави backup на etc директорията, permission-ите да са такива, че никой освен root да не може да ги чете
   и час от името на архивите да е името на машината а другата част да е в ISO формат.



    start 
    eb63 90 	- eb - jump to 63 , 90 - нищо не прави, Nope Command
    4-те последни реда от MBR HEX са за partition-ите и затова не може да има повече от 4 primary partitions

    C H S - цилиндър , глава , сектор - триизмерната геометрия

****** HW какво значат последните 4 реда като символи от MBR
	- показват инфо къде започват primary partition-ите и информация за тях.

  Partition tables
    - Master boot record (MBR) table structure
	- primary partitions (max 4)
	- extended partition (max 1)
	- logial partitions 
	- max number of partitions limited by kernel and tools 
	- 32 bit LBA limits max disk size to 2TB
    - GUID Partition Table (GPT) Structure (part of EFI)
	- 128 partitions
	- No extended or logical partitions
	- Critical structures duplicated and CRC checked
	- 64bit LBA limits max disk size to 8 ZB ((2^64-1)*512)

  Swap Partition
    - стои в отделен partition
    - няма нужда от допълнителен abstraction layer
    

  Swap 
    ------- прегледай man
    - 0x82		- така се записва в паметта че е swap partition
    - mkswap(8)		- sets up a Linux swap area on a device or in a file (not recomended).
			- The  device  argument  will  usually  be a disk partition (something like /dev/sdb7) but can also be a file.
    - swapon(8) / swapoff(8) - enable/disable devices and files for paging and swapping
    - free(1) 		- Display amount of free and used memory in the system
    - top(1)		- процесите
    - vmstat(8)		- Report virtual memory statistics
    - /proc/meminfo

    - ex - 
      maistora@bt:~$ vmstat 1 100	- показва инфо 100 пъти през 1 секунда

  Filesystems
    - Containment 
    - IO
    - Mount options
    - Filesystem level backup and restore
    - Separation of user and system

  Filesystems
    - Filesystem Planning 
      - /		- на един партитион
      - /boot		- тук седи kernel-а и някои конфигурационни файлове - да се отделя в първия partition на диска който е 128 мб
      - swap		- стандартно е да се сложи като отделен partition
      - /var
      - /tmp
      - /usr		- трудно може да се отдели в отделна файлова система
      - /home		- стандартно е да се сложи като отделен partition
      - /opt
   - In root - /enc, /bin, /sbin, /lib, /dev

  Partitioning disks
    ---------------- 
    * fdisk(8) - докато не изпълним командата write нищо не е записано. Инструмент за промяна на partition таблицата. Няма общо с файловата система. Не поддържа GPT partition таблици.
      - create/edit DOS/MBR & SUN/BSD disklabels
      - 16/63 partitions
      - in memory, from disk (/proc/partitions)
      - update kernel structures (partprobe) 	- кара kernel-а да препрочете конфигурацията и да ъпдейтне промените. По принцип кернела не засича промените след write. Трябва му reboot
      - types (83, 82, fd, 8e, 05, ee)		- флагчета за partition-и. Може да видим какво значат чрез -> fdisk /dev/sda1 -> l
    * sfdisk(8)	- scriptable disk
    - fdisk и sfdisk - могат само да създават и премахват partition-и

    * parted(8)
      - supports many disklabel types (including DOS and GPT)
      - writes changes to disk immediately
      - can move and resize partitions and filesystems

      maistora@bt:~$ fdisk -l /dev/sda

      Disk /dev/sda: 250.1 GB, 250059350016 bytes
      255 heads, 63 sectors/track, 30401 cylinders
      Units = cylinders of 16065 * 512 = 8225280 bytes
      Sector size (logical/physical): 512 bytes / 512 bytes
      I/O size (minimum/optimal): 512 bytes / 512 bytes
      Disk identifier: 0x39f47e90

	Device Boot      Start         End      Blocks   Id  System
      /dev/sda1   *           1        6374    51197952   83  Linux
      /dev/sda2            6375       27695   171260932+   7  HPFS/NTFS
      /dev/sda3           27696       30248    20505600   83  Linux
      /dev/sda4           30249       30401     1228972+  82  Linux swap / Solaris


от /dev/sda1 до /dev/sda4 са само за primary partitions

    Filesystem creation 
      - mkfs.ext2
      - mkfs.ext3
      - mkfs.ext4
      - mkfs.jts
      ????????

    Filesystem support
      - Minix, ext2, MS-DOS, UMSDOS, VFAT, NTFS, NFS, ISO9660,
	HPFS, SYSV, SMB, AFFS, BeFS, BFS, EFS, NWFS, QNX, RFS, UDF, UFS
      - Support for advanced logging / journaling systems
	- ReiserFS, ext3, JFS, XFS, Reiser4
	- ext3/ext4
	* cat /proc/filesystems

   Selecting filesystem
    - ext2
    - ext3	- stable, It is more fragmentation-prone that EXT4 and XFS and it is very slow in creating/deleting large amount of files
    - ext4	- 
    - ReiserFS
    - XFS
    - JFS
    - ZFS
    - Btfs - best for fragmentation
****** HW - коя за какво е полезна
EXT3/4 are the best choice, followed by BTRFS and, at last place, XFS.


  Filesystem features
    - Standard Unix filesystem 
      - singly rooted
      - case sensitivity
      - long file names
      - support links
      - ctime, atime, mtime
    ???????????????????????



----------------------------------------------------------------------------- 03.12.2011                                                     
                                             
Filesystem creation

Filesystem creation with mkfs –t filesystem_type
-	mkfs.ext2
-	mkfs.ext3
-	mkfs.ext4
-	mkfs.jfs
-	mkfs.reiserfs
-	mkfs.xfs
-	mkfs.msdos


Filesystem support

•	Support for dozens of filesystem types including:
		-Minix, ext2, MS-DOS, UMSDOS, VFAT, NTFS, NFS, ISO9660, HPFS, SYSV, SMB, AFFS, BeFS, EFS, NWFS, ONX, RFS, UDF, UFS
•	Support for advanced logging/journaling  filesystems:
		-ReiserFS, ext3, JFS, XFS, Resiser4
		-ext3/ext4
		-cat  /proc/filesystems


Selecting filesystem
•	ext2
•	ext3
•	ext4
•	ReiserFS – журнална файлова система
•	XFS
•	JFS
•	ZFS
•	Btrfs


Filesystem maintenance

•	dumpe2fs(8) – dump ext2/ext3/ext4 information
•	tune2fs(8) – tunable parameters on ext2/ext3/ext4
•	e2label(8) – change the label on an ext2/ext3/ext4
•	fsck(8) – check and repair a Linux filesystem
•	e2fsck(8) – check a Linux ext2/ext3/ext4
•	debugfs(8) - ext2/ext3/ext4 debugger
•	findfs(8) – find a filesystem by UUID or label


Mounting filesystems

•	mount(8)
•	umount(8)
•	fstab(5)
•	fuser(1) – identify processes, that use files/sockets
•	lsof(8) – list open files /показва всички файлове, които са отворени в момента в ОС/

•	cat  /etc/mtab – mounted filesystems table /дава списък на mount-ираните файлови системи/
•	/proc/mounts

•	mount [-t type] [-o option[,option[,…]]] [device] [dir]
•	/etc/fstab
•	currently mounted filesystems
•	-o
•	--bind
•	Options
•	umount [device|dir] 



/etc/fstab

На всеки ред има запис на точно една файлова система. Системите, които са  по-нагоре в дървото, трябва да са по-нагоре и в описанието на fstab.

defaults – системата се mount-ира с read и write права, опцията auto и други опции.

За да може обикновен user да работи с файловата система, в опциите трябва да пише user или users.

•	Contains information about filesystems
•	Which filesystems to mount and when
		-Order is significant
		-One filesystem per line
•	Options for mounting each filesystem
•	Used to mount filesystems at boot time (auto vs. noauto)
•	Requires root access unless the user or users options are used



Resizing filesystems

•	Modify partition sizes
		-fdisk
		-sfdisk
•	Modify filesystem sizes
		-ext2/3/4 – resize2fs
		-XFS – xfs_growfs
		-Reiserfs – resize_reiserfs
•	Modify both simulataneously
		-Parted




Persistent block devices

•	Block device names may change as a result of:
		-Hardware failure
		-Software configuration change
		-USB, Firewire, PCMCIA/Cardbus
•	Potential persistent naming solutions
		-Filesystem labels
		-UUID
		-UDEV



udev

•	Manages all device nodes on the system
•	/etc/udev/udev.conf
		-Main configuration file, which should never need any changes
•	/etc/udev/rules.d/*.rules
		-Files are evaluated in lexicographical order
•	Example udev rule:
		-SYBSYSTEM==”net”, ACTION==”add”, DRIVERS==”?*”, ATTR{address}==”9c : 8e : 99 : 3d : 53 : 7d”, ATTR{dev_id}==”0x0”, ATTR{type}==”1”, KERNEL==”eth*”, NAME=”eth0”
•	Information
		-udevadm  info  -a  --name=/dev/sda  

Домашно: 
1)	Да се прочете в man страницата за всичко описано във Filesystem maintenance
2)	Какво е mount  --bind
3)	Какви опции се поддържат за ext3/4 файлови системи

------------------------------------------------------------------------------------------- 03.12.2011
--------------------------------- записки от Диана Чанкова и Гергана Стойчева

----------03.12.2011----------- Д. Чанкова
Selecting filesystem
•    ext2 - не е журнална файлова система
•    ext3 - развива ext2
•    ext4 - features - multiblock allocation, jurnall checksum
•    ReiserFS – журнална файлова система, Ханс Рейзър
•    XFS - 64bits
•    JFS - създадена от IBM за AIX
•    ZFS - комбинирана файлова система 
•    Btrfs - B-tree filesystem, разработена от Oracle Corporation


Filesystem maintenance

•    dumpe2fs(8) – dump ext2/ext3/ext4 information
•    tune2fs(8) – tunable parameters on ext2/ext3/ext4
•    e2label(8) – change the label on an ext2/ext3/ext4
•    fsck(8) – check and repair a Linux filesystem
•    e2fsck(8) – check a Linux ext2/ext3/ext4			-r - This option does nothing at all; it is provided only for backwards compatibility.
•    debugfs(8) - ext2/ext3/ext4 debugger
•    findfs(8) – find a filesystem by UUID or label

** Задача 1 ** Създаване на нов партишън,файлова система и маунтване за мнт
създаваме нов дял на втория диск, който направихме мин. път ( от 100мб) - слава чрез 
fdisk /dev/sdb  и внимателно четем какво изписва на екрана (избираме букви -n,p, v, w. Много е важно да има v и w накрая за да се запише)
той ще бъде например с размер +10М
Задаваме тип на файловата система в новият дял, който създадохме. 
mkfs.ext4 /dev/sdb1
После го маунтваме за директория mnt чрез :
mount /dev/sdb1 /mnt
След рестартиране обаче всички тези хубави неща, няма да са валидни и за това :

**Задача 2 ** Целта е да се монтира за постоянно нашият партишън
Закачане на партишъна към директория в директория media
Четем съдържанието на файла fstab в etc. Този файл указва, къде да се mount-ват нещата.
grep -v ^# /etc/fstab където -v е инверсия и искаме да се покаже на екрана всичко без коментарите.
Отваряме си чрез vi fstab-а и записваме на последният ред :
/dev/sdb1    /media/new     ext4     default       0    2  !!разбира се предварително си създаваме директорията, към която монтираме

В този файл можем да задаваме това което монтираме също и чрез етикети и чрез UUID .
** ако не искаме в mount на устроиството да има аtime във ф.с. => tune2fs -m 0 /dev/sdb1 
е2fsck - !!разбирасе демонтираме и монтираме преди и след операцията

** слагане на етикет на партишън :
e2label /dev/sdb1 new

** търсене по етикети :
findfs LABEL=new

Mounting filesystems

•    mount(8)
•    umount(8)
•    fstab(5) - file system static information
•    fuser(1) – identify processes, that use files/sockets
•    lsof(8) – list open files /показва всички файлове, които са отворени в момента в ОС/
 Възможно е да тр да се инсталира.
•    cat  /etc/mtab – mounted filesystems table /дава списък на mount-ираните файлови системи/ Обновява се автоматично
•    /proc/mounts

•    mount [-t type] [-o option[,option[,…]]] [device] [dir]
•    /etc/fstab
•    currently mounted filesystems
•    -o
•    --bind
•    Options
•    umount [device|dir] 


/etc/mtab - за всички файлови системи
/etc/fstab - за текущо закачените файлови системи

На всеки ред има запис на точно една файлова система. Системите, които са  по-нагоре в дървото, трябва да са по-нагоре и в описанието на fstab.

defaults – системата се mount-ира с read и write права, опцията auto и други опции.

За да може обикновен user да работи с файловата система, в опциите трябва да пише user или users.
стойността на options в /etc/fstab   може да бъде user,noauto

•    Contains information about filesystems
•    Which filesystems to mount and when
        -Order is significant
        -One filesystem per line
•    Options for mounting each filesystem
•    Used to mount filesystems at boot time (auto vs. noauto)
•    Requires root access unless the user or users options are used



Resizing filesystems

•    Modify partition sizes
        -fdisk - показва дължината в партишън таблицата
        -sfdisk - използва параметри... - has four (main) uses: list the size of a partition, list the partitions on a device, check the partitions on a device, and - very
					  dangerous - repartition a device.

•    Modify filesystem sizes
        -ext2/3/4 – resize2fs
        -XFS – xfs_growfs
        -Reiserfs – resize_reiserfs
•    Modify both simulataneously
        -Parted




Persistent block devices

•    Block device names may change as a result of:
        -Hardware failure
        -Software configuration change
        -USB, Firewire, PCMCIA/Cardbus
•    Potential persistent naming solutions
        -Filesystem labels
        -UUID
        -UDEV

** Задача 3 ** Създаваме нов партишън и правим всички по-горни стъпки за монтиране. Задаваме чрез етикети монтираното в познатия файл :)
LABEL=nov    /media/new2     ext4     default       0    2
ако напишем df -h без да сме монтирали , няма да излезе нищо... => mount -a


udev

•    Manages all device nodes on the system
•    /etc/udev/udev.conf
        -Main configuration file, which should never need any changes
•    /etc/udev/rules.d/*.rules
        -Files are evaluated in lexicographical order
•    Example udev rule:
        -SYBSYSTEM==”net”, ACTION==”add”, DRIVERS==”?*”, ATTR{address}==”9c : 8e : 99 : 3d : 53 : 7d”, ATTR{dev_id}==”0x0”, ATTR{type}==”1”, KERNEL==”eth*”, NAME=”eth0”
•    Information
        -udevadm  info  -a  --name=/dev/sda 
	
Домашно: 
1)    Да се прочете в man страницата за всичко описано във Filesystem maintenance
2)    Какво е mount  --bind


    The bind mounts.
              Since Linux 2.4.0 it is possible to remount part of the file hierarchy somewhere else. The call is
                     mount --bind olddir newdir
              or shortoption
                     mount -B olddir newdir
              or fstab entry is:
                     /olddir /newdir none bind

              After this call the same contents is accessible in two places.  One can also remount a single file (on a single file).

              This call attaches only (part of) a single filesystem, not possible submounts. The entire file hierarchy including  submounts  is
              attached a second place using
                     mount --rbind olddir newdir
              or shortoption
                     mount -R olddir newdir

              Note  that the filesystem mount options will remain the same as those on the original mount point, and cannot be changed by pass‐
              ing the -o option along with --bind/--rbind. The mount options can be changed by a separate remount command, for example:

                     mount --bind olddir newdir
                     mount -o remount,ro newdir

3)    Какви опции се поддържат за ext3/4 файлови системи


--------------------------------------------------------------------------------------- G. Stoicheva

Filesystem creation

Filesystem creation with mkfs –t filesystem_type
-	mkfs.ext2
-	mkfs.ext3
-	mkfs.ext4
-	mkfs.jfs
-	mkfs.reiserfs
-	mkfs.xfs
-	mkfs.msdos


Filesystem support

•	Support for dozens of filesystem types including:
		-Minix, ext2, MS-DOS, UMSDOS, VFAT, NTFS, NFS, ISO9660, HPFS, SYSV, SMB, AFFS, BeFS, EFS, NWFS, ONX, RFS, UDF, UFS
•	Support for advanced logging/journaling  filesystems:
		-ReiserFS, ext3, JFS, XFS, Resiser4
		-ext3/ext4
		-cat  /proc/filesystems


Selecting filesystem
•	ext2
•	ext3
•	ext4
•	ReiserFS – журнална файлова система
•	XFS
•	JFS
•	ZFS
•	Btrfs


Filesystem maintenance

•	dumpe2fs(8) – dump ext2/ext3/ext4 information
•	tune2fs(8) – tunable parameters on ext2/ext3/ext4
•	e2label(8) – change the label on an ext2/ext3/ext4
•	fsck(8) – check and repair a Linux filesystem
•	e2fsck(8) – check a Linux ext2/ext3/ext4
•	debugfs(8) - ext2/ext3/ext4 debugger
•	findfs(8) – find a filesystem by UUID or label


Mounting filesystems

•	mount(8)
•	umount(8)
•	fstab(5)
•	fuser(1) – identify processes, that use files/sockets
•	lsof(8) – list open files /показва всички файлове, които са отворени в момента в ОС/

•	cat  /etc/mtab – mounted filesystems table /дава списък на mount-ираните файлови системи/
•	/proc/mounts

•	mount [-t type] [-o option[,option[,…]]] [device] [dir]
•	/etc/fstab
•	currently mounted filesystems
•	-o
•	--bind
•	Options
•	umount [device|dir] 



/etc/fstab

На всеки ред има запис на точно една файлова система. Системите, които са  по-нагоре в дървото, трябва да са по-нагоре и в описанието на fstab.

defaults – системата се mount-ира с read и write права, опцията auto и други опции.

За да може обикновен user да работи с файловата система, в опциите трябва да пише user или users.

•	Contains information about filesystems
•	Which filesystems to mount and when
		-Order is significant
		-One filesystem per line
•	Options for mounting each filesystem
•	Used to mount filesystems at boot time (auto vs. noauto)
•	Requires root access unless the user or users options are used



Resizing filesystems

•	Modify partition sizes
		-fdisk
		-sfdisk
•	Modify filesystem sizes
		-ext2/3/4 – resize2fs
		-XFS – xfs_growfs
		-Reiserfs – resize_reiserfs
•	Modify both simulataneously
		-Parted




Persistent block devices

•	Block device names may change as a result of:
		-Hardware failure
		-Software configuration change
		-USB, Firewire, PCMCIA/Cardbus
•	Potential persistent naming solutions
		-Filesystem labels
		-UUID
		-UDEV



udev

•	Manages all device nodes on the system
•	/etc/udev/udev.conf
		-Main configuration file, which should never need any changes
•	/etc/udev/rules.d/*.rules
		-Files are evaluated in lexicographical order
•	Example udev rule:
		-SYBSYSTEM==”net”, ACTION==”add”, DRIVERS==”?*”, ATTR{address}==”9c : 8e : 99 : 3d : 53 : 7d”, ATTR{dev_id}==”0x0”, ATTR{type}==”1”, KERNEL==”eth*”, NAME=”eth0”
•	Information
		-udevadm  info  -a  --name=/dev/sda  

Домашно: 
1)	Да се прочете в man страницата за всичко описано във Filesystem maintenance
2)	Какво е mount  --bind
3)	Какви опции се поддържат за ext3/4 файлови системи


-------------------------------------------------------------------------------------- 10.12.2011 + history file

  RAID Concepts
    - Compbining many physical devices into one logical device
    - Implement in software or hardware
    - Increase size
    - Increase performance
    - RAID-0 - получаваме от 2 диска един диск с обединено пространство
    - RAID-1 - 2 диска по 100 mb получаваме 2 диска по 100 с ендква информация
    - RAID-10 vs RAID-01 
      - RAID-10 - RAID едно + нула
	- Ако имаме 4 диска по 1 GB и ако направим RAID-10 означава че 2 от тези диска ще направим RAID-1 
	  и от останалите ще направим пак RAID-1 и от 2те двойки ще направим RAID-0 - имаме 2 ГБ
      - RAID-01 - RAID нула + едно
	- дисккове А, B, C, D - комбинираме А и В в RAID-0 и C и D в RAID-0 и 2те двойки в RAID-1

    - RAID-5 - прави баланс между RAID-0 и RAID-1 , ако от 3 диска гръмне един останалите 2 ще продължават да работят.
	      - Това става благодарение на правила за това от къде почва всеки диск, но ако гръмне един работи по-бавно.
	      - На 2 от дисковете се пише информация а на 3тия ще се запишат checksum-и
    - RAID-6 - 
    - http://en.wikipedia.org/wiki/Standard_RAID_levels		- чети подробно
    
    - Според Велин смисъл има само от RAID-1 и RAID-10 (чете се RAID десет или едно + нула)

    - може да имаме A, B, C в RAID-1 като C е в standby режим и не се ползва. Ако гръмне някой от А и В автоматично RAID-a почва да се rebuild-ва върху C. После може да си добави
      още един диск който да бъде в standby.

  Array Management
    * mdadm --help		-
    * partition FD
    * /etc/mdadm/mdadm.conf
    * /proc/mdstat

  За да си направим ping да работи във виртуалната машина:
	<сега default името на мрежовата карта ми е eth1 а трябва да е eth0 (защото на нея има настройките които се вземат от виртуалната машина)>
	* cd /etc/udev/rules.d/
	* ll
	* vi 70-persistent-net.rules
	* (от тук изтриваме голяма част от нещата до края на файла (shift+D + D))
	* reboot
	готово :)

    - apt-cache search mdadm -	 търси в името пакетите да има някъде mdadm 

  - задача 1 
    - създаваме 2 диска по 1 ГБ с по 4 partition-а, като ако имаме някакви записи които да се mount-ват ги махаме, изчистваме си partition table-а (всичко почваме на чисто)
  


  * mount -t vboxsf share mount_point  	- за монтиране на споделена папка между виртуалната машина и реалната машина. share е името на споделената папка.

  * mdadm
  
    искаме RAID между sdb1 и sdc1
  
  * mdadm --create /dev/md0 --level=1 --raid-devices=2 /dev/sd[bc]1
    
    преди да направим raid-а трябва да umount-нем sdb1 и sdc1
  * mdadm -Q --detail /dev/md0 		- за да видим детайли за райд-а


  * bc - някакъв конзолен калкулатор :))))
  
  * dd file1 file2 - чете от единия файл и пише в другия файл

  Logical Volume Manager
      -- ВАЖНО ЗА ИЗПИТА --

    - Physical Volumes (PV)	- всеки има даден брой extent-и  - това е едно блоково устройство
    - Physical Extents (PE) 	- върху него се създават различни структури, на които оказваме размера на парчетата
    - Volume Groups (VG)	- логическо обединение на 1 или повече physical volume-и. В рамките на 1 volume група extent size-a е еднакъв.
    - Logical Volumes (LV)	- от дадена volume група да използваме еди колко си extent-а
    - Logical Extents (LE)	- същото нещо като Physical extent - файловата система се прави върху него
    - Filesystems (FS)

  Creating VG
    - partition typCreate Physical e 8E
    - Create physical volumes
      * pvcreate /dev/device [device] [...]
    - Create Volume Group
      * vgcreate VGname /dev/device [device] [...]
    
  Creating Logical Volumes
    - Create Logiacal Volumes
      * lvcreate -l number_of_extents -n LVname VGname
      * lvcreate -L size -n LVname VGname
    - Create filesystems
      * mkfs -t file_system_type device
    - Mount the logical volume and test
      * /etc/fstab
      * mount -a

  Administration of LVM
    - Viewing 
      * pvdisplay, vgdisplay, lvdisplay, lvmdiskscan, pvs, vgs, lvs
    - Resizing 
      * lvreduce, lvextend, lvresize, vgreduce, vgextend, resize2fs (ext2/3)
    - Moving PVs and VGs
      * vgchange
      * vgexport, vgimport
      * pvmove

  Advanced LVM Concepts
    - Snapshots
      - Obtaining consistent backups
      * lvcreate -s | --snapshot
    - LVM Striping / Mirroring and RAID
      - Built-int striping and mirroring support
    - LVM in a clustering environment
      - GFS2 (Global filesystem version 2)
      - OCFS2, the Oracle Cluster File System
      - Lustre
  

  w3m gmail.com 	- bash browser :P

  
---------------------------------------------------------------------------- 17.12.2011 + history file

За да изтрием райд:
Fail all the devices, then remove them, then stop the raid. eg

mdadm --manage /dev/mdfoo --fail /dev/sdfoo
mdadm --manage /dev/mdfoo --remove /dev/sdfoo
mdadm --manage --stop /dev/mdfoo

Правилото:
Правилното предварително планиране предотвратява посраното пикливо подрискване

sfdisk -d /dev/sdb | sfdisk /dev/sdc		- Правим дъмп на конфигурацията на /dev/sdb като този дъмп го подаваме на входа на sfdisk с параметър /dev/sdc 
						  което фактически копира конфигурацията (примерно брой и големина на партишъните) на sdb върху sdc 

ДОМАШНО:
  LBA - какво е?
  Logical block addressing (LBA) is a common scheme used for specifying the location of blocks of data stored on computer storage devices, 
   generally secondary storage systems such as hard disks.
  LBA is a particularly simple linear addressing scheme; blocks are located by an integer index, with the first block being LBA 0, the second LBA 1, and so on.
  IDE standard included 22-bit LBA as an option, which was further extended to 28-bit with the release of ATA-1 (1994) and to 48-bit 
   with the release of ATA-6 (2003). Most hard drives released after 1996 implement logical block addressing.

  Linux boot process on x86
    - BIOS (Basic Input Output System) / POST (Power On Self Test)
    - MBR (Master Boot Record)
    - GRUB (Grand Unified Boot Loader)- стандартен BOOT LOADER в днешно време / LILO (Linux Loader) - по-стар
    - Linux kernel - 
    - root fs / initrd - 
    - /sbin/initrd - 

  LILO
    - list of available kernels / OS
    - LILO boot options
    - Kernel boot options 
    - ELILO has EFI support
    - /etc/lilo.conf
    - LILO is superseded by GRUB

  GRUB - по-гъвкав от LILO
    - list of available kernels / OS
    - fs support
    - int 13h - прекъсване на BIOS-a (ниско ниво)
    - serial console
    - interactive
    - boot options
    - /etc/default/grub
    - /etc/grub.d/*
    - /boot/grub/*

  Kernel boot parameters
    - http://www.tldp.org/HOWTO/BootPrompt-HOWTO.html
    - Any parameters not recognized are passed to init
    - /proc/cmdline
    - Kernel documentation

  // как се казва - 'Ubuntu, with Linux 2.6.39.4'
  menuentry 'Ubuntu, with Linux 2.6.39.4' --class ubuntu --class gnu-linux --class gnu --class os {
        autoexec=startx
        recordfail
        insmod ext2	- зарежда модул който да разпознава ext2 файлови системи
        set root='(hd0,1)' - указва къде е root fs-a 
        search --no-floppy --fs-uuid --set cb85e170-9e33-4b69-b4ce-9412448c46ed
        linux   /boot/vmlinuz-2.6.39.4 root=UUID=cb85e170-9e33-4b69-b4ce-9412448c46ed ro   text splash vga=791
        initrd  /boot/initrd.img-2.6.39.4
  }


  /sbin/init
    - first process launched by kernel
    - PID 1
    - All other processes are children of init
    - init=/path/to/executable
    - /etc/inittab


    - Ако по време на начално зареждане дадем init= до някакво binary то кернела ще 
      зареди въпросния executable вместо инит. 
      Най-интересни употреби:
	Ако "сме си забравили паролата" на нашия компютър 
	може да boot-нем примерно /bin/bash (вместо init), после remount-ваме файловата система 
	като wr (щото е било ro) след това можем да променим паролата на root и т.н. (devil).

  Init styles
    - BSD init - по-прост като конфигурационни файлове, но по-малко гъвкав
      - /etc/rc{,.conf}
    - SysV init - по-гъвкав, но по-сложен (уж) (стандартния начин за boot-ване)
      - runlevels
ДОМАШНО: проучи  тези:
    - Dependency based init (LSB - Linux standard base) - В отделните init сриптове има специална секция за него в която пише реда в  който ще се изпълняват скриптовете.
    - Event-driven (Upstart)
      - Ubuntu

  Runlevels - Даден таргет ... на операционната система
    - Даден набор от операции които трябва да са се случили
    // ДА ИЗЯДЕМ man за :
    * init(8)
    * inittab(8)
    - runlevel S	- ????
    - runlevel 0	- Дефинира последователност от действия които трябва да се случат при условие че изключваме ОС
    - runlevel 6	- ---- при условие че искаме да рестартираме
    - runlevel 1	- single-user runlevel - случва се в обратна посока; - нещо през което ще минеме докато стигнем
			  до runlevel S
    - multi-user runlevels 2-5

  * who -r - показва в кой runlevel сме в момента

  /etc/inittab
    - Default runlevel
    - One-time tasks
    - Start up services for a given runlevel (or the default)
    - Spawn /sbin/getty for tty1-6
      - Ако я нямаше конфиг. в този файл нямаше да можем да се логваме в текстова среда

  Init scripts
    - /etc/init.d/
    - /etc/rc{1,2,3,4,5,6,S}.d/
    - S##script - S за start ## - цифри - указват в какъв ред ще се извикат
    - K##script	- K за kill
    
    - /etc/init.d/rc
    - /etc/rc.local

  Managing Daemons
    - # /etc/init.d/daemon start
    - # /etc/init.d/daemon stop
    - restart, reload, status

  initrd
    

  Разгледай extend-ване на logical и physical volume

-----------------------------------------------------------------------------------------------07.01.2012 Д. Чанкова

Hardware & Kernel

dmesg(1) kernel съобщения
/var/log/dmesg
/var/log/messages
/proc/ and /sys/
	- proc/cpuinfo - подробности за процесофа
	- proc/pci
	- proc/interrupts

команди:
lspci(8) и lspci -v 
lsusb(8) закачени устройства
dmidecode(8) - запитвания на различни настр. за флагове
biosdecode(8) - | -
lshw (1) - дърво с hardware на мапнината (apt-get install)

USB configuration
udevd -на базата на правила и съобщения се създават

Chipset kernel modules
Device kernel modules
чипсетове за usb : xhci , ohci, uhci, whci, ehci

Device files and HW config
механизъм за комуникация

/dev/
mknod - пробинг на хард.
udev - динамично създ. на базата на правила
options to kernel
options to modules
Може динамично да се добавят модули на които да се задават опции за поведение.
/etc/modules
/etc/modprobe.d/* - зареждане на модули, кои, какви модули

Ако поддр. на устроиството не е на модули , се задават параметри на kernel-a

Kernel modules
modinfo (8)
lsmod(8)
insmod(8)
rmmod(8)
modprobe(8)- insmode-...
/lib/modules/$(uname -v)/modules.dep - кой модул от кой зависи
depmod(8)

/proc/ - (въртуална) има обекти с цифри; вътре има id-та
/proc/pid/
/proc/sys/ - контролира и променя kernel-a
	cat-четене
	echo - записва нещо
	sysclt - промяна на настройките от им. на пром. в /proc/sys/
/etc/sysctl.conf

/sys/ вирт., прем. от proc тук
provides hardware inf. needed bz udev
centralized location for device infor.
clean up /proc/
sysfs

/sys/block
/sys/bus/
/sys/class/
/sys/devices/
/sys/module

/sys/firmware/
/sys/kernel/
/sys/power/

Kernel source

-Master source repository for upstream
www.kernel.org 
full source

parch

gz/bz2/xz -3 вида архиви, съдържаши версии на кърнела;
 GPG- signed - подсигурява, че това, което сме
свалили е оригинално.
versioning - (най-чистият kernel - vanila kernel)
най-новият е 3.2; има различки в архитектурите между старите версии и 0.9 .. и другите
2.0.хх - номенклатура за стабилен (stable)кернел
2.1.yy - development и ако станат стабилни отиват в 2.0.xx дървото и после 2.2.xx 
и 2.3.yy; 2.4.xx и 2.5.yy, 2.6.хх се появяват допълнителни числа => 2.6.хх.yy(уу-sec.back портове)
и излезе 3.0.0
Мехнизмът че весията е различна е с AC3(производителна фирма) името - 2.4.16- AC1
2.6.38 - el.55 за redhat
преди е значело 24-> 2.6 че има ключови промени

Kernel config

/usr/src

make clean - почиства дървото
make e файл но почти като команда
make distclean - oще по-добре почиства
make mrproper -
make config - осиг. на интерфейс, през който се конфигурира
make menuconfig - подобно , но по-удобно
make xconfig/gconfig/qconfig - с графична среда се конфигурира
make oldconfig - от пред. версия на кърнела се взимат на стр. и само където има разлики
се създават въпроси.


- Kernel Component Categories
	-Ganeral Option
	- Processor tyoe and featues
 	- Networking
	- Device Drivers
	- File systems
	- Kernel hacking
	- Security options
* yes/ no vs yes/no/modules - как се показва дали има тези fatures

Compile and install

make - компилиране
-make modules-install
-/lib/modules/x.y.z/ -  копира ги вътре в тези структури и стоят модулите

Initial root filesystem image
-initrd, initramfs - запалване на ...
-mkinitrd, mkinitramfs

cp arch/i386/boot/bzImage копира се в boot-umlinux -z

Файлове :
-system.map
-config
-boot loader - конфигуриране на bootloader-а да зареди kernel-a

Задача :

-сваляме кърнела, разархивираме и компилираме 

>uname -r команда за вида на кърнела (2.6.32-5-686 версия)
>uname -a 
>file /boot/vmlinux-2.6.32.5
>ls /boot
	lspci -k | less
wget като apt-get install но от конкретния линк

>wget линк на кърнала от сайта им
>mv linux.... /usr/src
	du -h linux - важно е да се провери дали има място
>tar xvfj linux....
>du -sh linux-3.2
>прочитаме readme


>apt-get update| upgrade за да сме сигурни че всичко е актуално
>apt-get install libncurces5 -dev
		 libncursesw5 -dev
>make oldconfig
>make menuconfig
>make - create a compressed kernel image
и make install - възможно е....
.... <не го довършихме, защото беше баве процеса и нямаше време>




----------------------------------------------------------------------------------------------- 14.01.2012 
*.doc файл от Д. Серафимова


----------------------------------------------------------------------------------------------- 21.01.2012

Задача:
  Създадохме нова виртуална машина (8ГБ твърд диск, 512 мб оперативна памет). На нея трябва инсталираме най-новата Debian Stable, 
  да създадем LV-и на които да имаме / , /home , /tmp. След това да upgrade-нем към Testing Debian. 

Подход: 
  1. Изтеглихме .iso пакета (netinst) от ftp://ftp.uni-sofia.bg/debian.
  2. Стартирахме виртуалната машина като boot-ваме от .iso диска. 
  3. Избираме Advanced Installation (май така се казваше) и от там -> Expert Install.
  4. Караме стъпките една след друга като четем внимателно.
  5. Като стигнем до partition-инга за да осъществим разделянето (/,/home,/tmp) в logical volume-и трябва 
      тези logical volume-и да са в logical volume група а тя върху някакъв physical volume (напр. файлови системи, partition-и и т.н.). 
      Както всички си спомняме от преди за да може да LVM-а да запали logical volume групите той трябва да зареди от друг physical volume.
      За целта ще създадем 2 partition-a - на първия ще монтираме /boot (от където ще се палят logical volume-ите) а на другата ще монтираме /, 
      където ще бъде фактически LVG-ата и в нея ще създадем 3 + 1 logical volume-a (LV) ( + 1 е защото ще сложим и swap освен 3-те от задачата(/ , /home , /tmp.)).
      За /boot заделихме 128 мб, а за 2рия partition каквото остана. Форматираме с ext4. след като форматираме и 2та partition-a избираме опцията 
      LVM Configuration (или нещо такова). И там избираме 2рия partition. Избираме да създадем VG и след това запазваме. Избираме да създадем LV, форматираме и запазваме.
      Големината определихме така: ~4GB за / , ~1GB SWAP, ~1GB /home, ~2GB /tmp. 
      След като се върнем в менюто отново трябва да форматираме LV-ите (иначе не става, което пък довежда до въпроса има ли смисъл първоначалното им форматиране.). 
      Запазваме всичко и продължаваме инсталацията.
  6. За partition table type избрахме msdos (default-ното)
  7. Мрежата си я нагласихме чрез DHCP.
  8. За избор от къде да дърпа пакетите има 2 опции http и ftp (http избрахме)
  9. Избрахме GRUB.
  10. След като инстлирахме и създадохме някакви user-и velin ни накара да се разменим и да сменим паролите на другите(без да ги знаем). -> При зареждане на GRUB 
      натискаме "е" за да променяме конфигурацията. На реда kernel или linux накрая добавяме init=/bin/bash за да се пали bash-a при стартиране. След това boot-ваме. 
      След като boot-нем сме влезли в системата само с read права. Това трябва да се промени. За целта ще я демонтираме с read/write права. Това става чрез 
      ~> mount -n -o remount,rw / - фактически ре-монтираме руут файловата система. За повече инфо за mount в "man mount" :) . След това пишем едно 
      ~> passwd  и сме готови :).
      От това може да се защитим ако забраним достъп до /etc/shadows или /etc/passwd без root парола. 
      Това може да се разбие като boot-нем от CD, монтираме си файловата система и направим същата стъпка като преди малко.
      От това пък можем да се защитим ако забраним boot-ването на CD-та и тем подобни през BIOS (BIOS-а трябва да има парола).
      Това може да се разбие като извадим батерийката на motherboard-а и паролата изчезне ;)
      Най-сигурното е да си криптираме диска но тогава ще трябва всеки път да си пишем паролата като стартираме. 
      Това също може да се разбие ако "камериерката в хотела влезе докато ни няма, разглоби ни лаптопа, сложи един подслушвател и го сглоби. 
	Така ще разбере каква ни е била паролата"  :D 
  11. Трябва да upgrade-нем до testing версията. За целта променяме /etc/apt/sources.list като смняме имена на стабилната версия с имената на тестовата. 
	При нас стабилната беше sqeeze а тестовата съответна е wheezy и промените бяха:
	Oт:
	  deb http://ftp.uni-sofia.bg/debian/ squeeze main non-free contrib
	  deb http://ftp.uni-sofia.bg/debian/ squeeze-updates main non-free contrib
	  deb http://security.debian.org/ squeeze/updates main non-free contrib
	На:
	  deb http://ftp.uni-sofia.bg/debian/ wheezy main non-free contrib
	  deb http://ftp.uni-sofia.bg/debian/ wheezy-proposed-updates main non-free contrib
	  deb http://ftp.uni-sofia.bg/debian-security/ wheezy/updates main non-free contrib
	  deb http://security.debian.org/ wheezy/updates main non-free contrib
  12. Направихме apt-get update и после apt-get dist-upgrade.
  13. Чакане чакане. Изникна проблем, че процесора ни не подържа 686-pae, а досега е работил 
	с 686 (само, което вече се счита за толкова старо, че е причислено към 486 архитектурата). Предлага ни да изтрием 686 или 686-pae и да сложим 486. 
	Тогава ще трябва да прекомпилираме kernel-а. Понеже сме с виртуални машини velin реши че можем да минем само с една малка промяна. След приключване на 
	upgrade-a изключихме машините и дадохме опцията на процесора (Physical Volume Extension (PAE)) и стартирахме наново. Сега трябва да инсталираме едни header-и. 
	~> apt-cache search linux-headers
	~> apt-get install linux-headers-3.1.0-1-686-pae (или нещо такова - всичко до сега го пиша по спомен така че може малко да съм объркал на места)
	рестарт не помня дали не беше нужен но няма да навреди. 
      

Трябва да изчетем FAQ на debian.org -> http://www.debian.org/doc/manuals/debian-faq/
