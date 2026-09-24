# Linux Fundamentals

1. Files and Directories
pwd

Shows the current working directory.

pwd

Purpose: Used to check the location of the current directory.

ls

Lists the files and directories in the current directory.

ls

Purpose: Used to view available files and folders.

ls -la

Displays all files and directories, including hidden files, with detailed information.

ls -la

Purpose: Used to view file permissions, ownership, size, and hidden files.

mkdir security_lab

Creates a new directory named security_lab.

mkdir security_lab

Purpose: Used to create a new folder for storing security lab files.

cd security_lab

Moves into the security_lab directory.

cd security_lab

Purpose: Used to change the current working directory.

touch notes.txt

Creates an empty file named notes.txt.

touch notes.txt

Purpose: Used to create a new empty file.

echo "Linux Security Lab" > notes.txt

Writes the text into notes.txt.

echo "Linux Security Lab" > notes.txt

Purpose: Used to write text into a file. The > operator redirects the output to the file.

cat notes.txt

Displays the contents of notes.txt.

cat notes.txt

Purpose: Used to read and display the contents of a file.

2. Copy and Move Files
cp notes.txt notes_backup.txt

Creates a copy of notes.txt named notes_backup.txt.

cp notes.txt notes_backup.txt

Purpose: Used to copy files.

mv notes_backup.txt backup.txt

Renames notes_backup.txt to backup.txt.

mv notes_backup.txt backup.txt

Purpose: The mv command is used to move or rename files and directories.

3. Linux Permissions
ls -l

Displays detailed information about files, including their permissions.

ls -l

Purpose: Used to check file permissions, owner, group, file size, and modification time.

chmod 600 notes.txt
chmod 600 notes.txt
ls -l notes.txt

Meaning of 600:

Owner: Read + Write
Group: No permission
Others: No permission

The permission is represented as:

rw-------
chmod 644 notes.txt
chmod 644 notes.txt
ls -l notes.txt

Meaning of 644:

Owner: Read + Write
Group: Read
Others: Read

The permission is represented as:

rw-r--r--
Permission Summary
Permission	Value
Read	4
Write	2
Execute	1

Therefore:

600 = 6 (read + write) + 0 + 0
644 = 6 (read + write) + 4 (read) + 4 (read)
4. Users and Groups
whoami

Displays the username of the currently logged-in user.

whoami

Purpose: Used to identify the current user.

id

Displays the user ID (UID), group ID (GID), and groups associated with the current user.

id

Purpose: Used to view user and group identification information.

groups

Shows the groups to which the current user belongs.

groups

Purpose: Used to check the user's group memberships.

cat /etc/passwd | head

Displays the first few entries from the /etc/passwd file.

cat /etc/passwd | head

Purpose: The /etc/passwd file contains information about user accounts. head displays the first few lines.

cat /etc/group | head

Displays the first few entries from the /etc/group file.

cat /etc/group | head

Purpose: The /etc/group file contains information about groups configured on the Linux system.

5. Process Management
ps aux

Displays currently running processes along with information such as users, process IDs, CPU usage, and memory usage.

ps aux

Purpose: Used to view running processes and their resource usage.

top

Displays running processes in real time.

top

Purpose: Used to monitor CPU usage, memory usage, processes, and system activity.

To exit top, press:

q
ps -ef

Displays all running processes in a detailed format.

ps -ef

Purpose: Used to view processes, their process IDs, parent process IDs, users, and commands.
