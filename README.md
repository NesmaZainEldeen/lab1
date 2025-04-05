# lab1
1. Install Ubuntu [Multipass]
   
3. What is the difference between rm and rmdir using man?
rm is to delete directories that have files and rmdir is for deleting empty directory

5. Create the following hierarchy under your home directory:
ubuntu@eternal-sole:~$ mkdir dir1
ubuntu@eternal-sole:~$ cd dir1
ubuntu@eternal-sole:~/dir1$ mkdir dir11
ubuntu@eternal-sole:~/dir1$ mkdir dir12
ubuntu@eternal-sole:~/dir1$  cd dir11
ubuntu@eternal-sole:~/dir1/dir11$ touch file1
ubuntu@eternal-sole:~/dir1/dir11$ cd
ubuntu@eternal-sole:~$ ls
dir1
ubuntu@eternal-sole:~$ mkdir docs
ubuntu@eternal-sole:~$ cd docs
ubuntu@eternal-sole:~/docs$ touch mycv
ubuntu@eternal-sole:~/docs$ cd
ubuntu@eternal-sole:~$ ls
dir1  docs

a. Remove dir11 in one-step. What did you notice? And how did you overcome that?
ubuntu@eternal-sole:~$ cd dir1
ubuntu@eternal-sole:~/dir1$  rm -r dir11

b. Then remove dir12 using rmdir –p command. State what happened to the
ubuntu@eternal-sole:~/dir1$ rmdir -p dir12
ubuntu@eternal-sole:~/dir1$ cd docs
-bash: cd: docs: No such file or directory
ubuntu@eternal-sole:~/dir1$ ls

c. The output of the command pwd was /home/user.
ubuntu@eternal-sole:~/dir1$ cd ..
ubuntu@eternal-sole:~$ cd docs
ubuntu@eternal-sole:~/docs$ pwd mycv
absolute
/home/ubuntu/docs
ubuntu@eternal-sole:~/docs$ cd
ubuntu@eternal-sole:~$ pwd mycv
relative 
/home/ubuntu

5. Copy the /etc/passwd file to your home directory making its name is mypasswd.
ubuntu@eternal-sole:~$  cd ..
ubuntu@eternal-sole:/home$ cd ..
ubuntu@eternal-sole:/$ cd etc
ubuntu@eternal-sole:/etc$ sudo cp passwd mypasswd

6. Rename this new file to be oldpasswd.
ubuntu@eternal-sole:/etc$ sudo mv mypasswd oldpasswd

7. You are in /usr/bin, list four ways to go to your home directory
ubuntu@eternal-sole:/etc$ cd ..
ubuntu@eternal-sole:/$ cd usr
ubuntu@eternal-sole:/usr$ cd bin
ubuntu@eternal-sole:/usr/bin$ cd
ubuntu@eternal-sole:~$ cd usr
ubuntu@eternal-sole:~$ cd ..
ubuntu@eternal-sole:/home$ cd ..
ubuntu@eternal-sole:/$  cd usr
ubuntu@eternal-sole:/usr$ cd bin
ubuntu@eternal-sole:/usr/bin$ cd ~
ubuntu@eternal-sole:~$ cd ..
ubuntu@eternal-sole:/home$ cd ..
ubuntu@eternal-sole:/$ cd usr
ubuntu@eternal-sole:/usr$ cd bin
ubuntu@eternal-sole:/usr/bin$ cd /home/ubuntu
ubuntu@eternal-sole:~$ cd ..
ubuntu@eternal-sole:/home$ cd ..
ubuntu@eternal-sole:/$ cd usr
ubuntu@eternal-sole:/usr$ cd bin
ubuntu@eternal-sole:/usr/bin$ cd $HOME
ubuntu@eternal-sole:~$ cd
ubuntu@eternal-sole:~$ cd usr
-bash: cd: usr: No such file or directory
ubuntu@eternal-sole:~$ cd ..
ubuntu@eternal-sole:/home$ cd ..

8. List Linux commands in /usr/bin that start with letter w
ubuntu@eternal-sole:/$ cd usr
ubuntu@eternal-sole:/usr$ cd bin
ubuntu@eternal-sole:/usr/bin$ ls | grep ^[w]
w
wall
watch
watchgnupg
wc
wdctl
wget
whatis
whereis
which
which.debianutils
whiptail
who
whoami
wifi-status
write

9. Display the first 4 lines of /etc/passwd
ubuntu@eternal-sole:/usr/bin$ cd
ubuntu@eternal-sole:~$ cd ..
ubuntu@eternal-sole:/home$ cd ..
ubuntu@eternal-sole:/$ cd etc
ubuntu@eternal-sole:/etc$ head -n 4 /etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin

10.Display the last 7 lines of /etc/passwd
ubuntu@eternal-sole:/etc$ tail -n 7 /etc/passwd
sshd:x:105:65534::/run/sshd:/usr/sbin/nologin
pollinate:x:106:1::/var/cache/pollinate:/bin/false
tcpdump:x:107:108::/nonexistent:/usr/sbin/nologin
landscape:x:108:109::/var/lib/landscape:/usr/sbin/nologin
fwupd-refresh:x:990:990:Firmware update daemon:/var/lib/fwupd:/usr/sbin/nologin
polkitd:x:989:989:User for polkitd:/:/usr/sbin/nologin
ubuntu:x:1000:1000:Ubuntu:/home/ubuntu:/bin/bash

11.Display the man pages of passwd the command and the file sequentially in one command.
ubuntu@eternal-sole:/etc$ man 1 passwd && man 5 

12.Display the man page of the passwd file.
ubuntu@eternal-sole:/etc$ man 5 passwd

13.Display a list of all the commands that contain the keyword passwd in their man page.
ubuntu@eternal-sole:/etc$ man -k passwd
chgpasswd (8)        - update group passwords in batch mode
chpasswd (8)         - update passwords in batch mode
fgetpwent_r (3)      - get passwd file entry reentrantly
getpwent_r (3)       - get passwd file entry reentrantly
gpasswd (1)          - administer /etc/group and /etc/gshadow
grub-mkpasswd-pbkdf2 (1) - generate hashed password for GRUB
openssl-passwd (1ssl) - compute password hashes
pam_localuser (8)    - require users to be listed in /etc/passwd
passwd (1)           - change user password
passwd (1ssl)        - OpenSSL application commands
passwd (5)           - the password file
passwd2des (3)       - RFS password encryption
pwhistory_helper (8) - Helper binary that transfers password hashes from passwd or shadow to opasswd
update-passwd (8)    - safely update /etc/passwd, /etc/shadow and /etc/group
ubuntu@eternal-sole:/etc$ cd

14. Using vi write your CV in the file mycv. Your CV should include your name, age, school,
college, experience,...
ubuntu@eternal-sole:~$ cd docs
ubuntu@eternal-sole:~/docs$ vi mycv
name:nesma
age:22
school:cu
College:cs
experience:fresh grad

15. Open mycv file using vi command then: Without using arrows state how to:
a. Move the cursor down one line at time.
j
b. Move the cursor up one line at time.
k
c. Search for word age
/age
d. Step to line 5 (assuming that you are in line 1 and file is more than 5 lines).
5(g+shift)
e. Delete the line you are on and line 5.
dd on the same line and :5d for line 5
f. How to step to the end of line and change to writing mode in one-step.
$

16. st the available shells in your system.
ubuntu@eternal-sole:~/docs$ cd
ubuntu@eternal-sole:~$ cd ..
ubuntu@eternal-sole:/home$ cd ..
ubuntu@eternal-sole:/$ cd etc
ubuntu@eternal-sole:/etc$ cat /etc/shells
# /etc/shells: valid login shells
/bin/sh
/usr/bin/sh
/bin/bash
/usr/bin/bash
/bin/rbash
/usr/bin/rbash
/usr/bin/dash
/usr/bin/screen
/usr/bin/tmux
