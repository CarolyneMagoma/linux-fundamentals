# Linux-Fundamentals

# PART 1 - File Management.

# Task 1 - Create Project Structure

On this task we were to create a structure of directories log, backup,script,configs, and temp.

![alt text](/screenshots/image1.png)

# Task 2 -Create Files

on this task, we created files on the logs,scripts, and config directories.
on these Directories we created the app.log, deploy.sh and app.conf files as shown on the diretory tree below.

![alt text](image2.png)


# Task 3 - Add Sample Content

On app.log file we added some contents.

INFO Server started
WARNING Disk almost  full
ERROR Database connection failed
INFO User login successful

# Task 4 - Copy Backup

we created a backup of app.conf file in the configs folder to backup directory,
to create a backup we used the "cp" command 

![alt text](image3.png)


# PART 2 -File Viewing & Log Investigation
# Task 5 - Investigate Logs
 
This task wanted us to investigate the logs file that we created and find the errors and warning entries. we used the "find" command to do this.

find . -name "app.log" -exec grep -n "warning" {} \; 

find . - search from current directory
-name "app.log" - locate the file by name
-exec -execute a command on the found file
grep "ERROR" - searches for ERROR entries
{} - represents the found files
\; - ends the execute statement.

![alt text](image4.png)

we searched the warning entries on the app.log file. 

![alt text](image5.png)


# Task 6 - Monitor Logs Live

In this task we used the command "tail -f app.log " and added aome content to that file as we can see the content is being monitored in real life.

![alt text](image6.png)


# PART 3 - Permissions & Ownership
# Script Permissions

In this task we have to change permissions for deploy.sh file to make it executable.

for permissions we always have the read, write and execute permissions.

we used the "chmod +x deploy.sh" this gives the file the execute command.


# Task 8 - Secure Config File (configs/app.conf)

We gave this file the read and write permissions by running the "chmod 600 app.conf" command.
![alt text](image7.png)








