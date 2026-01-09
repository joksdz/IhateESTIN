## Computers : 
a computer system is the set of hardware and software its main task is to perform input of info processing and storing  the info and outputting it  
**software** : 
programs that are stored and executed on a computer system , this includes the os(which manages and controls the hardware resources ) 

**hardware** : 
 the physical components of a computer system that you can see and touch . 
 ![[Pasted image 20260107180316.png]]
 
## OS : 
An operating system (OS) is the set of programs responsible for the link between the hardware resources of a computer and the apps i.e software . 
ex : windows , macos , linux (arch btw , android 
![[Pasted image 20260107165748.png]]


so the OS is basically like is an intermediate between the hardware and the rest of the softwares 
### Windows VS Linux  : 
![[Pasted image 20260107165918.png]]
### the functionality of an OS :
- info management 
- program execution 
- memory management 
- access rights management 


### single/ multi user/task systems :
user :
- single user : is an os where only one user can access the os at a time 
- mutli user : allows several users to access the system at the same time 
task : 
- A single-task operating system is one that manages only one task at a time (a single program). When the program is launched, the operating system is only allowed to launch another program at the end of execution, or in the event of an error.
 - multitask : allows for multiple programs to run at the same time  
## characteristics of Unix  : 
- multi-platform : independent of hardware
	- time sharing multitasking : multitasking is ensured by a preemptive mechanism = system authoritatively interrupts the task currently being executed to  the next one 
- multi users: this is managed by the access rights mechanism applying to all resources managed by the system 
### Unix users : 
- Each resource (file, directory, program, etc.) is the property of a user registered on the machine
- Each person accessing the system has a user name (login) and a password
- each users has an id
ex: ![[Pasted image 20260107174021.png]]
- each user has permissions (access rights) x, r ,w 
- each user has a reserved dir (workspace) in home where he has all the rights for the files in there 
- a user can add access to other users 
 ![[Pasted image 20260107174345.png]]
### User Groups : 
for selective sharing of hardware with others , each user can be a member of one or more user groups 
- the group is identified by its id (GID ) 
- each file has one or more groups 
- the user that owns the file can allow others to access it 
### SuperUser (sudo):
 for a multiuser os we have to provide a super user or a root that has all the permissions to everything on the system 
 ![[Pasted image 20260107174835.png]]

### main functions : 
- resource sharing : fair between the processes 
- uses special files to access hardware resources (hardisks , flash drives ) 
- memory management 
- file management 
![[Pasted image 20260107175348.png]]
### the structure of the Unix system
- **the kernel** : the fundamental element of the os , it ensures :
	 - the management of resources
	 - communication between hardware and software 
	 - management of different software : launching apps and stuff 
- **Shell**: UNIX command interpreter (analyze executes and return the response) , the shell sends sys calls to the kernel based on the user requests 
- **Utilities**: basic services to users like the interface , editors compilers... 
- **Applications**: user programs 
![[Pasted image 20260107175942.png]]
## Linux session types :

### text mode : 
command line mode that has the advantage of preserving commands history and useful for quick editing 

### graphical mode : 
the gui allows users to quickly interact with applications and navigate websites more efficiently . it provides visual elements such as icons ,buttons and menus.... 



to switch between the graphical mode and the text mode by using the combinations : ($\sum^6_{i=1} , CTRL + ALT + F_i$ )(you like that ? )

## Piping : 
first | next  basically takes the output of the first and gives it as the input of the next


![[Pasted image 20260107233008.png]]
## command chaining: 
this can be achieved with ";" so you do : 
> cmd1 ; cmd2 ;cmd3 

 if an error happens it still executes whats after the panicking command 
### AND : 
using && stops when an error happens it executes the first and the second if there is no problems 
### OR : 
using || for this one the second executes if the first fails , meaning if the first works then it executes it and stops without doing the second one 
### Grouping 
(cmd1;cmd2;cmd3) this will treat the output as a singe thing so we can redirect it using > to file.txt
we can replace the ; with && or || 

![[Pasted image 20260107235420.png]]

### nesting : 
$(cmd)
it executes the command and returns the result 

## redirection: 
 \> redirects output to file (stdout to screen by default )
 2> redirects errors (stderr same)
 &> redirects both to the same file  
if the file you are redirecting to doesnt exist then it will create and save to it
if it exits it will overwrite it
use >> so you dont delete the content of those files
< is for input redirection ( the pipe is better since this one just usually take the file names and not command returns )
# Directories and files :
in Unix everything is a file 
A file can:
- Contain data
- Be a link to another file
- Serve as an access method to a device (memory, screen, HDD, ...)
-  Provide a means of communication between processes
## types of files : 
- normal files : contains data like text or smth 
- directory files : contains a list of  to other linux files 
- special files : refer to devices , input/output devices (terminal , drives) 
- symbolic link files : files pointing to other files 
## naming : 
file names are limited to 255 characters 
files starting with a . are hidden 
the file size are unlimited 
naming should consist of s: A-Z, a-z, 0-9, ‘\_’, ‘-‘, and ‘.' 
avoid this :  !, &, (), ', “, <>, $, ? ... 
## file access : 
. refers to the current dir 
.. refers to prv dir 
the root dir : 
![[Pasted image 20260108014850.png]]
## access paths : 
a file is id'ed by its access path (position in the hierarchy)
and manipulated by its path ,the path consists of the list of dirs traversed and terminates by the current file name 
### types : 
#### Absolute : 
starts from root home user so : /home/user/...
#### relative paths : 
based on the working dir so from my pc rep/c/Calculator_c is a relative path 
you can use ../../smth to go backwards twice then to smth 
the command tree : its like ls visualizer use -L n to specify the level of branching 
## Inodes :
The inode contains all the necessary information concerning the file, except its name:
o File type: regular file, directory, symbolic link, etc.
o Owner, access rights to the file.
o Number of physical links.
o UID (User ID).
o GID (Group ID).
o Size of the file in bytes.
o Dates (creation, access, modification).
o References to the data blocks.
the number that ls -i prints is only a ref for the inode table 
## file storage : 
a directory is a file that stores the name of files and their inode number 
 ![[Pasted image 20260108022044.png]]

## Links : 
a link is a ref to an existing file or dir



### types : 
#### hard links (physical) : 
less used . same content same inode can have diff name 
how to make : ln file linkName
cant be used on dir 
#### symbolic links : 

can be used on dirs 
depends on their target 
the symbolic link points to the file name and not to the inode directly 
![[Pasted image 20260108022557.png]]
how to make : ln -s file LinkName
symbolic link can ref a file on a diff partition , and when deleting the target the data is freed 

# Metacharacters(wildcards):
## \* : 
anything 
so rm -rf ilove* , will include ilovecandy iloveyou iloveher... 
rm -rf \*s* includes anything that has an s init either from the start or the end or anywhere inside of it 
## ? : 
one character that can be anything non empty 
rm -rf iloveh?r will include , iloveher iloveh3r...
## \[] :
this means like or but it does both like : 
rm -rf iloveh[e3]r , will remove iloveher iloveh3r...
this is set form 
the interval form is : 
	iloveher[1-9] so this will remove anything with iloveher and a  number at the end 

\[!] means not whats inside 
 ls a[!a-z]b.txt aZb.txt,  this will delete anything that starts with a and ends with b.txt and doesnt have a lowercase character in it 
## user rights : 
there are three categories : user-group-other
there are three types of right read-write-execute 
the first letter indicates the file type either - for normal , d for dir , l for link 
to change permissions : 
chmod : 
has two methods : 
symbolic : 
(u,g,o,a)(+/-)(r,w,x) 
numeric methods: 
(octal): chmod 657 file

chmod [who] op [permissions] file/directory (that is the syntaxe) , where :
 who (optional): indicates which classes are affected by chmod, consisting of one
or more letters (u, g, o) or for all categories.
op:
![[Pasted image 20260108024434.png]]
![[Pasted image 20260108024430.png]]![[Pasted image 20260108024445.png]]


Numeric method L represents each 3 permissions by a number 0 to 7  1 in allowed rihgts and 0 in not allowed 
![[Pasted image 20260108024625.png]]