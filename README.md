# Lab1_Linux
# 4. Create the following hierarchy under your home directory:

# a. Remove dir11 in one-step. What did you notice? And how did you overcome that?
# b. Then remove dir12 using rmdir –p command. State what happened to the hierarchy 


    ubuntu@festive-screamer:~$ mkdir dir1/dir11
    ubuntu@festive-screamer:~$ mkdir dir1/dir12
    ubuntu@festive-screamer:~$ mkdir docs
    ubuntu@festive-screamer:~$ touch docs/mycv
    ubuntu@festive-screamer:~$ touch dir1/dir11/file1
    ubuntu@festive-screamer:~$ ls
    dir1  docs
    ubuntu@festive-screamer:~$ ls dir1
    dir11  dir12

    ubuntu@festive-screamer:~$ cd dir1
    ubuntu@festive-screamer:~/dir1$ rm dir11
    rm: cannot remove 'dir11': Is a directory
    ubuntu@festive-screamer:~/dir1$ rm -r dir11
    ubuntu@festive-screamer:~/dir1$ rmdir -p dir12

# c. The output of the command pwd was /home/user. Write the absolute and relative path for the file mycv

    ubuntu@festive-screamer:~/docs$ pwd
    /home/ubuntu/docs
    ubuntu@festive-screamer:~/docs$ readlink -f mycv
    /home/ubuntu/docs/mycv

#5. Copy the /etc/passwd file to your home directory making its name is mypasswd.
#6. Rename this new file to be oldpasswd.

    ubuntu@festive-screamer:/$ sudo cp etc/passwd mypasswd
    ubuntu@festive-screamer:/$ sudo mv mypasswd oldpasswd


#7. You are in /usr/bin, list four ways to go to your home directory
#8. List Linux commands in /usr/bin that start with letter w


    ubuntu@festive-screamer:/$ cd bin
    ubuntu@festive-screamer:/bin$ cd ..
    ubuntu@festive-screamer:/$ cd home
    
    
    ubuntu@festive-screamer:/home$ cd ..
    ubuntu@festive-screamer:/$ cd bin
    ubuntu@festive-screamer:/bin$ ls |grep ^[w]
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

#9. Display the first 4 lines of /etc/passwd
    
    ubuntu@festive-screamer:/$ head -4 etc/passwd
    
    root:x:0:0:root:/root:/bin/bash
    daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
    bin:x:2:2:bin:/bin:/usr/sbin/nologin
    sys:x:3:3:sys:/dev:/usr/sbin/nologin

#10.Display the last 7 lines of /etc/passwd

    ubuntu@festive-screamer:/$ tail -7 etc/passwd
    
    sshd:x:105:65534::/run/sshd:/usr/sbin/nologin
    pollinate:x:106:1::/var/cache/pollinate:/bin/false
    tcpdump:x:107:108::/nonexistent:/usr/sbin/nologin
    landscape:x:108:109::/var/lib/landscape:/usr/sbin/nologin
    fwupd-refresh:x:990:990:Firmware update daemon:/var/lib/fwupd:/usr/sbin/nologin
    polkitd:x:989:989:User for polkitd:/:/usr/sbin/nologin
    ubuntu:x:1000:1000:Ubuntu:/home/ubuntu:/bin/bash

#11.Display the man pages of passwd the command and the file sequentially in one command.
#12.Display the man page of the passwd file.

    ubuntu@festive-screamer:/$ man 1 5 etc/passwd
    ubuntu@festive-screamer:/$ man 5 etc/passwd

![WhatsApp Image 2025-04-05 at 15 40 20_f719e7ff](https://github.com/user-attachments/assets/6ad6793b-d3de-40d5-b830-9904de66dc76)

![WhatsApp Image 2025-04-05 at 15 42 58_3488082d](https://github.com/user-attachments/assets/7d3377e7-c5e7-45ff-bcdc-4268a52ab2b9)

# 13.Display a list of all the commands that contain the keyword passwd in their man page.
    ubuntu@festive-screamer:/$ man -k etc/passwd
    
    pam_localuser (8)    - require users to be listed in /etc/passwd
    update-passwd (8)    - safely update /etc/passwd, /etc/shadow and /etc/group

#14. Using vi write your CV in the file mycv. Your CV should include your name, age, school, college, experience,...

    ubuntu@festive-screamer:/$ sudo vi mycv

![WhatsApp Image 2025-04-05 at 20 13 47_2180165f](https://github.com/user-attachments/assets/b4b902a4-f061-4b3c-b6c1-0f10bbabd877)


#15. Open mycv file using vi command then: Without using arrows state how to:
#a. Move the cursor down one line at time.
#b. Move the cursor up one line at time.
#c. Search for word age

        /age
![WhatsApp Image 2025-04-05 at 20 14 52_d284e11e](https://github.com/user-attachments/assets/97c1ec7b-94bd-489b-96ec-a0510b969080)


#d. Step to line 5 (assuming that you are in line 1 and file is more than 5 lines).

    5G

#e. Delete the line you are on and line 5.
![WhatsApp Image 2025-04-05 at 20 15 47_45bd287a](https://github.com/user-attachments/assets/0636e2df-dfbd-404c-a384-13d2eba861d1)

#f. How to step to the end of line and change to writing mode in one-step.
![WhatsApp Image 2025-04-05 at 20 16 13_c89e3123](https://github.com/user-attachments/assets/e6764e96-8759-47c3-8704-a4df1bcf5b7c)


#16. st the available shells in your system.

    ubuntu@festive-screamer:/$ cat /etc/shells

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
