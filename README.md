# Linux Server Admin Lab on AWS EC2

Hands-on practice of Linux sysadmin tasks on an Ubuntu server on AWS EC2.

## Goal
Learn file management, logging, file permissions, and basic monitoring on a real cloud server.

## Environment
- AWS EC2 (Ubuntu), connected via EC2 Instance Connect
- Region: ap-south-1 (Mumbai)

## What I practiced

### 1. File and directory management
`mkdir`, `cd`, `pwd`, `touch`, `echo`, `ls -l`, `cat`

### 2. Logging with redirection
- `>` overwrites a file
- `>>` appends to a file

### 3. File permissions (chmod)

| Command | Permissions | Meaning |
|---|---|---|
| chmod 600 secret.txt | rw------- | Only the owner can read and write |
| chmod 621 secret.txt | rw--w---x | Owner: read/write, group: write, others: execute |
| chmod 746 secret.txt | rwxr--rw- | Owner: full, group: read, others: read/write |

Lesson: 600 is the right choice for confidential files. 746 even lets other users write to the file.

### 4. System monitoring
`date`, `uptime` (how long the server has been running), `free -h` (memory), `df -h` (disk space). Output was saved to `application.log` using `>>`.

## Skills
Linux CLI, file permissions, output redirection, AWS EC2
