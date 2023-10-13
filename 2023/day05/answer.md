# Day 5 Task: Advanced Linux Shell Scripting with User management

## Write a bash script create directories.sh that when the script is executed with three given arguments (one is the directory name and second is start number of directories and third is the end number of directories ) it creates a specified number of directories with a dynamic directory name.

#!/bin/bash

`check if three arguments are given`

if [ "$#" -ne 3 ]; then
echo "Usage: ./directories.sh <directory-name> <start-number> <end-number>"
exit 1
fi

` get the three arguments`

dir_name=$1
start_num=$2
end_num=$3

` create directories`

for ((i=$start_num; i<=$end_num; i++)); do
mkdir "$dir_name$i"
done

echo "Directories created successfully!"

## Create a Script to backup all your work done till now.

#!/bin/bash

`` Define backup directory and filename`

backup_dir="/path/to/backup/directory" e.g /home/vijay/linux
backup_filename="work_backup\*$(date +'%Y%m%d%H%M%S').tar.gz"

`Create the backup`

tar -czvf "$backup_dir/$backup_filename" /path/to/source/directory e.g /home/vijay/angular

` Check if the backup was successful`

if [ $? -eq 0 ]; then
echo "Backup completed successfully."
echo "Backup saved as: $backup_dir/$backup_filename"
else
echo "Backup failed."
fi

## Read About Cron and Crontab, to automate the backup Script

Cron and crontab are tools used to automate tasks on Unix-like operating systems, including scheduling the execution of scripts on a regular basis.

`Cron`:

1. Cron is a time-based job scheduler in Unix-like operating systems.
2. It allows you to schedule tasks (scripts or commands) to run at specific times or intervals.
3. Cron jobs are defined in a file called a "crontab."

`Crontab`:

1. A crontab is a configuration file that specifies the schedule of tasks to be run by the cron daemon.
2. Each user can have their own crontab, and there's a system-wide crontab as well.

Cron Syntax:

Cron jobs are defined using a specific syntax in a crontab file. The syntax consists of five fields, followed by the command or script to run. Each field represents a unit of time.
The fields are, in order: minute (0-59), hour (0-23), day of the month (1-31), month (1-12), and day of the week (0-7, where both 0 and 7 represent Sunday).

An asterisk (\*) can be used as a wildcard to match all values. For example, an asterisk in the minute field means "every minute."
Here's how you can use crontab to automate your backup script:

For example, if you want to run your backup script every day at 2 AM, add this line:

0 2 \* \* \* /path/to/your/backup_script.sh

The 0 in the first field represents the minute (run at the start of the hour).
The 2 in the second field represents the hour (2 AM).
The \* in the remaining fields means "every day of the month," "every month," and "every day of the week."

Your backup script will now run automatically every day at 2 AM.

## User Management

User management in Linux involves creating, modifying, and managing user accounts. It includes authentication, group management, access control, and privileges. User management is crucial for maintaining security and controlling access to resources on a Linux system.

## Create 2 users and just display their Usernames

To create two user accounts and display their usernames, you can use the useradd command to create the users and the cut command to extract and display their usernames from the /etc/passwd file.

# Create User1

sudo useradd User1

# Create User2

sudo useradd User2

# Display their usernames

grep -E "User1|User2" /etc/passwd | cut -d: -f1
