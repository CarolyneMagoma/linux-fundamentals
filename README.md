# Linux-Fundamentals

# PART 1 - File Management.

# Task 1 - Create Project Structure

On this task we created a structure with log, backup,script,configs, and temp directories

![alt text](/screenshots/image1.png)

# Task 2 -Create Files

On the Directories we created earlier the app.log, deploy.sh and app.conf were created on there respective directories as shown on the directory tree below.

![alt text](/screenshots/image2.png)


# Task 3 - Add Sample Content

On app.log file we added some contents.

INFO Server started \
WARNING Disk almost  full \
ERROR Database connection failed \
INFO User login successful \

# Task 4 - Copy Backup

We created a backup of app.conf file in the configs folder to backup directory,
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
![alt text](/screenshots/image.png)

# Task 16 - Verify Listening Ports
we used the command ss -tulnp to verif listening ports

![alt text](/screenshots/image-1.png)

# PART 6 - SSH & SCP
# Task 17 - Remote Access (Local to Remote)

![alt text](/screenshots/image-2.png)
![alt text](/screenshots/image-3.png)


# Task 18 -Secure  File Transfer

![alt text](/screenshots/image-4.png)
![alt text](/screenshots/image-5.png)

# Task 19 - Retrieve File (Remote to Local)

![alt text](/screenshots/image-6.png)

![alt text](/screenshots/image-7.png)

# PART 7 - Disk & System  Information

# Task 20 - Check  System Resources 
memory usage
![alt text](/screenshots/image-8.png)
Disk usage
![alt text](/screenshots/image-9.png)
uptime
![alt text](/screenshots/image-10.png)
linux version
![alt text](/screenshots/image-11.png)

# Task 21 - Analyze Storage
![alt text](/screenshots/image-12.png)
![alt text](/screenshots/image-13.png)


# PART 8 - Compression & Backup

# Task 22 - Create Backup Archive

![alt text](/screenshots/image-14.png)

# Task 23 - Extract

![alt text](/screenshots/image-15.png)


# LINUX_LAB

![alt text](image.png)


# PART 1 - FIND COMMAND

# Task 1 
in this task we have been asked to find all the .log files that we created at the beginning of the lab, we were to use the find command to do so.

![alt text](/screenshots/lab_screensots/image1.png)

# PART 2 - LOCATE COMMAND
# Task 3
we are to use the locate command to find a file auth.log

![alt text](/screenshots/lab_screensots/image4.png)
# PART 3 - GREP COMMAND
# Task 4

In this task we are to find error message in app.log file.

![alt text](/screenshots/lab_screensots/image2.png)

# Task 5
we are to find the warning text inside the app.log file.
![alt text](/screenshots/lab_screensots/image3.png)

# Task 6

we are to count the number of errors using the wc command by piping

![alt text](/screenshots/lab_screensots/image5.png)

![alt text](/screenshots/lab_screensots/image6.png)

# PART 4 - AWK COMMAND

# Task 7
on this task we are to print the timestamp in the file app.log file. 

![alt text](/screenshots/lab_screensots/image7.png)

# Task 8

# Task 9

On this task we rae to extract disk usage percentage from system.log

![alt text](/screenshots/lab_screensots/image8.png)

# PART 5 - PIPING

# Task 10

![alt text](/screenshots/lab_screensots/image9.png)

# Task 11

![alt text](/screenshots/lab_screensots/image10.png)

# Task 12

![alt text](/screenshots/lab_screensots/image11.png)

# PART 6 - XARGS

# Task 13

![alt text](/screenshots/lab_screensots/image12.png)

# Task 14


# Task 15


# ADVANCED CHALLENGE

The server is unstable.
identify disk issue

