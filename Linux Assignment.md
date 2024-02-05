# **Assignment 4**

> **1.** Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.

```
ayan@Sudo:~$ mkdir MyFiles
ayan@Sudo:~$ cd MyFiles
ayan@Sudo:~/MyFiles$ ls
ayan@Sudo:~/MyFiles$
```

> **2.** Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."

```
ayan@Sudo:~$ touch doc.txt
ayan@Sudo:~$ cp doc.txt MyFiles/
ayan@Sudo:~$ cd MyFiles
ayan@Sudo:~/MyFiles$ ls
doc.txt
ayan@Sudo:~/MyFiles$ mkdir Documents
ayan@Sudo:~/MyFiles$ mv doc.txt Documents
ayan@Sudo:~/MyFiles$ ls Documents
doc.txt
```

> **3.** Create an empty file named "notes.txt" in the "MyFiles" directory. Afterward, delete the file.

```
ayan@Sudo:~/MyFiles$ touch notes.txt
ayan@Sudo:~/MyFiles$ ls
Documents  notes.txt
ayan@Sudo:~/MyFiles$ rm notes.txt 
ayan@Sudo:~/MyFiles$ ls
Documents
```

> **4.** Create a hard link named "hardlink.txt" for the file "document.txt" within the "Documents" subdirectory. Also, create a symbolic link named "symlink.txt" in the same location.

```
ayan@Sudo:~/MyFiles$ cd Documents
ayan@Sudo:~/MyFiles/Documents$ ls
doc.txt
ayan@Sudo:~/MyFiles/Documents$ ln doc.txt hardlink.txt
ayan@Sudo:~/MyFiles/Documents$ ls
doc.txt  hardlink.txt
```

> **5.** In the "MyFiles" directory, use a single command to list all files that start with the letter "a" and have a ".txt" extension.

```
ayan@Sudo:~/MyFiles$ ls ./a*.txt
ls: cannot access './a*.txt': No such file or directory
ayan@Sudo:~/MyFiles$ cd Documents
ayan@Sudo:~/MyFiles/Documents$ ls ./a*.txt
ls: cannot access './a*.txt': No such file or directory
ayan@Sudo:~/MyFiles/Documents$ ls ./*.txt
./doc.txt  ./hardlink.txt
```

> **6.** Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.

```
ayan@Sudo:~/MyFiles/Documents$ ls
doc.txt  hardlink.txt
ayan@Sudo:~/MyFiles/Documents$ sudo rename 's/\.txt$/.bak/' *.txt
ayan@Sudo:~/MyFiles/Documents$ ls
doc.bak  hardlink.bak
```

> **7.** Use a wildcard character to copy all files from the "Documents" subdirectory of "MyFiles" to another directory named "Backup."

```
ayan@Sudo:~/MyFiles$ mkdir Backup
ayan@Sudo:~/MyFiles$ ls
Backup  Documents  hardlink.txt
ayan@Sudo:~/MyFiles$ cp Documents/* Backup
ayan@Sudo:~/MyFiles$ ls Backup
doc.bak  hardlink.bak
ayan@Sudo:~/MyFiles$ ls Documents
doc.bak  hardlink.bak
```

>**8.** Execute the ls command to list files in the current directory. Save the output to a file named "file_list.txt." Then, use a pipe to filter the output through grep to display only files with a ".txt" extension.

```
ayan@Sudo:~$ ls >file_list.txt
ayan@Sudo:~$ ls
'All Gates.sim1'   mpv-shot0001.jpg
 Arduino           Music
 Circuit.sim1      MyFiles
 Circuit.simu      Pictures
 Desktop           Public
 doc.txt           snap
 Documents         Templates
 Downloads         Videos
 file_list.txt
ayan@Sudo:~$ cat file_list.txt | grep '\.txt$'
doc.txt
file_list.txt
```

> **9.** Create a new text file named "my_notes.txt" using the touch command. Open the file in the Vim editor, add some text, and save the changes.

```
![Alt text](<Screenshot from 2024-02-03 21-00-38.png>)
```

> **10.** Run the date command and store the output in a variable named "current_date." Display the value of the variable and append it to the "my_notes.txt" file.

```

```

> **11.** Edit the Bash startup script (e.g., .bashrc) to set an environment variable named "CUSTOM_PATH" to a specific directory path. Ensure the variable is available in new shell sessions.

```

```

>**12.** Use the echo command to add a new line of text to the "my_notes.txt" file without overwriting existing content. Verify that the new text is appended.

```
ayan@Sudo:~$ find ./my_notes*.txt
./my_notes.txt
ayan@Sudo:~$ cat my_notes.txt
fosteringlinux
ayan@Sudo:~$ echo KeenAble >>my_notes.txt 
ayan@Sudo:~$ cat my_notes.txt 
fosteringlinux
KeenAble
```

> **13.** List all files in the "/etc" directory, filter the output to include only those containing the word "conf," and save the result to a file named "conf_files.txt."

```
ayan@Sudo:~$ sudo find /etc -type f -name *conf* > 
conf_files.txt
ayan@Sudo:~$ ls
'All Gates.sim1'   doc.txt         my_notes.txt
 Arduino           Documents       Pictures
 Circuit.sim1      Downloads       Public
 Circuit.simu      file_list.txt   snap
 conf_files.txt    Music           Templates
 Desktop           MyFiles         Videos
```

>**14.** Open the "my_notes.txt" file in Vim. Use Vim's search and replace functionality to replace all occurrences of the word "important" with "critical." Save the changes.

```
ayan@Sudo:~$ vim my_notes.txt

![Alt text](<Screenshot from 2024-02-04 17-36-25-1.png>)
```

>**15.** Create a new user account named "john_doe." Set the user's home directory to "/home/john_doe" and assign the user to the "users" group.

```
ayan@Sudo:~$ sudo useradd -m -d /home/john_doe john_doe
[sudo] password for ayan: 
ayan@Sudo:~$ sudo passwd john_doe 
New password:
passwd: password updated successfully
ayan@Sudo:~$ sudo usermod -aG users john_doe 
```

>**16.** Add the user "john_doe" to the sudoers file, allowing them superuser privileges. Confirm that "john_doe" can execute commands with sudo.


```
ayan@Sudo:~$ sudo visudo
ayan@Sudo:~$ sudo echo "Hello, I have sudo privileges!"
Hello, I have sudo privileges!
ayan@Sudo:~$ su - john_doe 
Password: 
su: Authentication failure
ayan@Sudo:~$ su - john_doe 
Password: 
$ apt update
Reading package lists... Done
```

>**17.** Modify the user account "john_doe" to change the default shell to "/bin/bash" and set the account's expiration date to one month from today.


```
ayan@Sudo:~$ sudo chsh -s /bin/bash john_doe 
[sudo] password for ayan: 
ayan@Sudo:~$ sudo chage -E$(date -d '+1month' +%d-%m-%Y) john_doe 
ayan@Sudo:~$ 
```

>**18.** Create a new group named "development_team." Add "john_doe" to this group and verify the group's existence.


```
ayan@Sudo:~$ sudo groupadd development_team
ayan@Sudo:~$ sudo usermod -aG development_team john_doe 
ayan@Sudo:~$ grep development_team /etc/group
development_team:x:1002:john_doe
```

> **19.** Remove "john_doe" from the "users" group and add them to the "development_team" group. Confirm the changes.

```
ayan@Sudo:~$ sudo deluser john_doe users
info: Removing user `john_doe' from group `users' ...
ayan@Sudo:~$ sudo usermod -aG development_team john_doe 
ayan@Sudo:~$ groups john_doe 
john_doe : john_doe development_team
```

>**20.** Delete the user account "john_doe" and ensure that their home directory is also removed.


```
ayan@Sudo:~$ sudo userdel -r john_doe 
userdel: user john_doe is currently used by process 16134
ayan@Sudo:~$ ^C
ayan@Sudo:~$ sudo pkill -u john_doe
ayan@Sudo:~$ sudo kill -9 16134
ayan@Sudo:~$ sudo userdel -r john_doe 
userdel: john_doe mail spool (/var/mail/john_doe) not found
ayan@Sudo:~$ ^C
ayan@Sudo:~$ ls /home/john_doe
ls: cannot access '/home/john_doe': No such file or directory
```

>**21.** Delete the group "development_team" and ensure that all users previously belonging to the group are appropriately handled.

```
ayan@Sudo:~$ grep development_team /etc/group
development_team:x:1002:
ayan@Sudo:~$ sudo deluser 1002 development_team
[sudo] password for ayan: 
fatal: The user `1002' does not exist.

ayan@Sudo:~$ sudo gpasswd -d 1002 development_team 
Removing user 1002 from group development_team
gpasswd: user '1002' is not a member of 'development_team'
ayan@Sudo:~$ sudo groupdel development_team 
ayan@Sudo:~$ grep development_team /etc/gr
groff/  group   group-  grub.d/ 
ayan@Sudo:~$ grep development_team /etc/group
ayan@Sudo:~$ 
```

>**22.** Implement a password policy that requires users to change their passwords every 90 days. Apply this policy to all existing and new user accounts.

```
sudo chage -M 90 -E $(date -d '+90 days' +%d-%m-%Y) -I -1 -m 7 -W 7 username
```
```bash
chage to change age or expiry
M for maximum psswrd age(90)
E for expiration date(after 90)
I for inactivity period to -1 for no inactivity
m for min no of days b/w psswd change
W for warning period
```

> **23.** Manually lock the user account "john_doe." Attempt to log in as "john_doe" to confirm that the account is locked. Then, unlock the account.

```
user john_doe has already been deleted
```

>**24.** Use the id command to display detailed information about the "john_doe" user, including user ID, group ID, and supplementary groups.

```
ayan@Sudo:~$ id ayan 
uid=1000(ayan) gid=1000(ayan) groups=1000(ayan),4(adm),20(dialout),24(cdrom),27(sudo),30(dip),46(plugdev),122(lpadmin),135(lxd),136(sambashare)
```

>**25.** Configure the password aging for the user "john_doe" to enforce a maximum password age of 60 days. Confirm that the changes take effect.

```

```