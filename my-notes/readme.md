# Linux Notes

All my notes related to Linux


- `ls` = list files in a directory
- `ls-a` = list all files including hidden files 

Hidden files have a period at the start example: .numan 

- `grep` = searches for a argument within a file. So grep "hello" file.txt woud try to find the word hello in file.txt
- `touch` = create a file
- `mkdir` = make a new directory. A directory is like a folder and this would contain files.
- `rm`
- `echo` = prints something to the terminal. Can also input text in a file by doing `echo "example text" > filename.txt`

The shell is what translates for the human to the computer and vice versa. The shell runs programs (called commands) and these are found in the binary. The binary is the compiled file of the programs.
You can have different shells such as zsh which is quite popular

- `>>` = this is called append operator. You can use `echo "example text 1" >> filename.txt` which will add a line of this text, and not overwrite.
- `cat` = this commands does a few different thing. It can read the contents of a file. Can also combine contents of two or more files into a new file. Example, `cat test.txt test2.txt > test3.txt`

- `head` and `tail` = these help to find lines within a file. head without anything specified shows the first 10 and tails shows the bottom 10. But you can combine both to find a specific amount of lines 
but head would tend to be a larger number than tail for accurate result. Also use the '|' which is called pipe. This command helps with combining both the 'head' and 'tail' command and is very useful in terms of searching through logs.

- `cp` = copy a file contents to another. cp file filetocopyto. `cp -r` does the same for directories, wont replace anything. just literally copies a folder to another folder


- `mv` = this can move or rename a file. renaming would be in the same directory. Example 'mv test.txt test1.txt'. And moving would be from one directory to another

- `rm` = remove/delete a file. use -r flag to remove a directory
- `rmdir` = removes a directory but must be empty. Use rm -r if directory not empty, to delete content too

- if there is a space within a file/folder name, use "" to pass as argument otherwise can cause issues

- vim is a text editor. 3 modes, command, insert, (?). i to enter insert, esc key to escape. save with :wq!

sudo is the super user - needed for some operations



# Users and Groups 

- `sudo - su` = this swithces you to the actual root user. Complete permissions over everything. Careful not to run `rm -rf /` as this deletes **EVERYTHING**. If you use without the hypen, it will switch but keep the current shell, so cant really do much

- var/log/auth.log has the logs of what root user and/or sudo has done previously. Good for security

- `sudo adduser (name of user)` = this creates a new user. Change their password with sudo passwd (name of user)

- `sudo groupadd (groupname)` = creates a new group
- `sudo usermod -aG (groupname) (username)` = this adds a user to a group you name
- etc/group contain all the groups of users. 

