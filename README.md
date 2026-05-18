# Linux-Fundamentals

# PART 1 - File Management.

# Task 1 - Create Project Structure

On this task we were to create a structure of directories log, backup,script,configs, and temp.

![alt text](/screenshots/image1.png)

# Task 2 -Create Files

on this task, we created files on the logs,scripts, and config directories.
on these Directories we created the app.log, deploy.sh and app.conf files as shown on the diretory tree below.

![alt text](/screenshots/image2.png)


# Task 3 - Add Sample Content

On app.log file we added some contents.

INFO Server started
WARNING Disk almost  full
ERROR Database connection failed
INFO User login successful

# Task 4 - Copy Backup

we created a backup of app.conf file in the configs folder to backup directory,
to create a backup we used the "cp" command 

![alt text](/screenshots/image3.png)


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

![alt text](/screenshots/image4.png)

we searched the warning entries on the app.log file. 

![alt text](/screenshots/image5.png)


# Task 6 - Monitor Logs Live

In this task we used the command "tail -f app.log " and added aome content to that file as we can see the content is being monitored in real life.

![alt text](/screenshots/image6.png)


# PART 3 - Permissions & Ownership
# Script Permissions

In this task we have to change permissions for deploy.sh file to make it executable.

for permissions we always have the read, write and execute permissions.

we used the "chmod +x deploy.sh" this gives the file the execute command.


# Task 8 - Secure Config File (configs/app.conf)

We gave this file the read and write permissions by running the "chmod 600 app.conf" command.

![alt text](/screenshots/image7.png)

# Task 9 - Explain Permissions

Explain:
755 - this means that the owner of the file has full permissions, the group has the read and execute permissions and the other users also have the read and execute permissions.
644 - this shows that the ownner has the read and write permissions, the group and other users have the read permissions only.
600 - this illustrates that the owner of the file has the read ans write permissions and the rest of the user have no permissions to perform any action.

# PART 4 - Process Management
# Task 10 - Start Background Process 

We have created a process on the background by running "sleep 500 &".

![alt text](/screenshots/image8.png)


as we can see on the image below, the process was created.

![alt text](/screenshots/image9.png)



# Task 11 - Identify Process

In this task we have to find the process ID(PID) and the process name. we used the command "ps aux | grep sleep "
from the results we can see the process ID is "11666i" and the process name is "sleep"

![alt text](/screenshots/image10.png)



# Task 12 - Terminate Process

we  have to stop the sleep process we created earlier, we use the kill -9 <process id> command.

# Task 13 - Monitor System
 
By using the top command we are able to see the total number of processes the cpu usage and memeory usage.

![alt text](/screenshots/image11.png)

# PART 5 - Networking & Connectivity

# Task 14 - Find Server IP
By the use of "ip a" command we are able to see an ip address 
![alt text](/screenshots/image12.png)

To see the hostaneme of the server we are using we run the command "hostname"

![alt text](/screenshots/image13.png)


# Task 15 - Test Connectivity
To test our linux machine internet access we pinged the google.com domain and as we can see it reachable sonce we have response from that domain.
![alt text](image.png)

# Task 16 - Verify Listening Ports
we used the command ss -tulnp to verif listening ports

![alt text](image-1.png)

# PART 6 - SSH & SCP
# Task 17 - Remote Access (Local to Remote)

![alt text](image-2.png)
![alt text](image-3.png)


# Task 18 -Secure  File Transfer

![alt text](image-4.png)
![alt text](image-5.png)

# Task 19 - Retrieve File (Remote to Local)

![alt text](image-6.png)

![alt text](image-7.png)
# PART 7 - Disk & System  Information

# Task 20 - Check  System Resources 
memory usage
![alt text](image-8.png)
Disk usage
![alt text](image-9.png)
uptime
![alt text](image-10.png)
linux version
![alt text](image-11.png)

# Task 21 - Analyze Storage
![alt text](image-12.png)
![alt text](image-13.png)


# PART 8 - Compression & Backup

# Task 22 - Create Backup Archive

![alt text](image-14.png)

# Task 23 - Extract

![alt text](image-15.png)


# LINUX_LAB

![alt text](image.png)


# PART 1 - FIND COMMAND

# Task 1 
in this task we have been asked to find all the .log files that we created at the beginning of the lab, we were to use the find command to do so.

![alt text](image.png)




