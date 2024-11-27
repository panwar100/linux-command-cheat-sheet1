# linux-command-cheat-sheet1
This repository contains a comprehensive guide to common Linux commands with examples and screenshots. It's designed to help users quickly reference essential commands for navigating, managing files, and configuring the system in a Linux environment.

## Table of Contents

1. [User Prompt](#1-rootlocalhost-)
2. [PWD](#2-pwd)
3. [CD](#3-cd)
4. [Date and Cal](#4-date-and-cal)
5. [Hostnamectl](#5-hostnamectl)
6. [LS Command](#6-ls)
7. [Mkdir and Rmdir](#7-mkdir-and-rmdir)
8. [Init Commands](#8-init-commands)
9. [Create File](#9-create-file)
10. [Overwrite or Create File (cat >)](#10-create-or-overwrite-a-file)

## 1) `root@localhost ~#` Explanation

This prompt represents the following:
- **root**: You are logged in as the root user, which has full administrative privileges.
- **localhost**: The hostname is set to localhost, the default for systems without a unique name.
- **~**: The home directory of the root user (`/root`).
- **#**: Indicates you are logged in as the root user (a `$` would indicate a non-root user).

![Screenshot from 2024-11-27 19-06-29](https://github.com/user-attachments/assets/6512f1ad-c230-4944-be37-f26ef8e6b6d3)

## 2) `pwd` Command

The `pwd` command prints the current working directory.
![Screenshot from 2024-11-27 19-10-32](https://github.com/user-attachments/assets/c1952a62-aa24-4500-9d67-ae78983eadc7)

## 3) `cd` Command

The `cd` command allows you to change directories.
![Screenshot from 2024-11-27 19-14-03](https://github.com/user-attachments/assets/d7df1475-782f-4945-a157-114d87a2a522)

### Going Up One Level:
The `cd ..` command takes you to the parent directory.
![Screenshot from 2024-11-27 19-17-09](https://github.com/user-attachments/assets/f9c55c03-342a-436d-bc44-efebf22c746b)

## 4) `date` and `cal` Commands

- **`date`**: Displays the current system date and time.
![Screenshot from 2024-11-27 19-19-18](https://github.com/user-attachments/assets/cc68c494-e4e3-414e-921c-d9ba152a33d6)

- Example variants: `+%a`, `+%A`, `+%x`, `+%X`, `+%h`, `+%H` for various formats.
![Screenshot from 2024-11-27 19-36-15](https://github.com/user-attachments/assets/4efe1eea-13d2-49e6-a892-1b0fcfd6b19f)

- **`cal`**: Displays a calendar in the terminal.
 
![Screenshot from 2024-11-27 19-22-16](https://github.com/user-attachments/assets/cef418ec-b4d6-4fe6-8821-349a52154003)
![Screenshot from 2024-11-27 19-23-23](https://github.com/user-attachments/assets/a1f5ff37-95ce-4162-886a-48fb525bf0db)

- View calendar for a specific year or past/future months.

![Screenshot from 2024-11-27 19-25-59](https://github.com/user-attachments/assets/50c0125f-e37c-4208-aadf-3fe4fecbfc49)

## 5) `hostnamectl` Command

Use `hostnamectl` to manage the system's hostname and related settings.

![Screenshot from 2024-11-27 19-42-31](https://github.com/user-attachments/assets/d348f883-7ec3-4a65-bd0d-16d74a2ec4df)

- To set a new hostname, use `hostnamectl set-hostname <hostname>`.

![Screenshot from 2024-11-27 19-50-00](https://github.com/user-attachments/assets/c44666e2-f1a2-488e-89f1-5f9dafca55d6)

then type bash or rebot system for refresh

## 6) `ls` Command

The `ls` command lists directory contents.

![Screenshot from 2024-11-27 19-51-22](https://github.com/user-attachments/assets/a9291459-7ce5-42b0-a82b-7cce67ce4ae7)

### Long Format:
The `ls -l` command shows detailed information about files and directories:
- File Permissions
- Number of Links
- Owner and Group
- File Size
- Last Modification Time
- File/Directory Name

![Screenshot from 2024-11-27 19-55-12](https://github.com/user-attachments/assets/977f00dd-9d37-4714-bd7b-24abe4ab81ce)

Hidden Files:
To list hidden files, use `ls -a`.

![Screenshot from 2024-11-27 20-01-11](https://github.com/user-attachments/assets/db674b23-3e88-42ba-80f2-ac96f9d8d93e)

## 7) `mkdir` and `rmdir` Commands

- **`mkdir`**: Creates directories.
  - Example: `mkdir -p j/k/l` creates nested directories `j/k/l`.
  - Example: `mkdir ab{1..10}` creates directories `ab1`, `ab2`, ..., `ab10`.

- **`rmdir`**: Removes directories (only empty directories).

![Screenshot from 2024-11-27 20-29-41](https://github.com/user-attachments/assets/7d9fd05f-4c28-49d3-9500-b6aa8d2ef0c8)
![Screenshot from 2024-11-27 20-31-30](https://github.com/user-attachments/assets/679cf1ec-229e-4f78-8e7f-2edd9d2579b4)
![Screenshot from 2024-11-27 20-44-46](https://github.com/user-attachments/assets/d8d1ba81-257a-4cba-bb84-fc153968cbe8)

where cd ../.. command in Linux is used to move up two levels in the directory structure from your current location

![Screenshot from 2024-11-27 20-47-44](https://github.com/user-attachments/assets/7f5d36cf-bf35-429c-98d6-4aa6ae16ebb0)
- remove the directory j and all its contents (including subdirectories and files)

![Screenshot from 2024-11-27 20-50-32](https://github.com/user-attachments/assets/b43e4263-2401-407e-8946-6d62b6adc8fa)

where   
-  -r: This option stands for recursive removal. It tells rm to delete directories and their contents recursively, including all files and subdirectories inside j.
-  -v: This option stands for verbose. It tells rm to display what it's doing, printing each file and directory it removes.
-  -f: This option stands for force. It forces rm to remove files and directories without prompting for confirmation, even if the files are write-protected or if the directory is not empty.

-Remove all files and directories (including hidden ones, if .* is used) in the current directory.

![Screenshot from 2024-11-27 20-55-04](https://github.com/user-attachments/assets/f8bec158-9518-465f-ad09-5f4e6c01c470)


## 8) `init` Commands

- **`init 0`**: Shuts down the system.
- **`init 6`**: Reboots the system.

## 9) Create File

Use commands to create files in Linux.

![Screenshot from 2024-11-27 21-09-58](https://github.com/user-attachments/assets/ac1f8fc7-bf39-42d9-89ef-cddcc759cf39)

## 10) `cat >` Command

The `cat >` command allows you to create or overwrite a file and input text interactively.
- To exit and save, press `Ctrl+D`.
- note: use cat and less for read the content inside the file
![Screenshot from 2024-11-27 21-12-15](https://github.com/user-attachments/assets/34e5b451-5d8a-4996-827b-3de1f426023d)

## Conclusion

This cheat sheet covers some of the most essential Linux commands to navigate the file system, manage files, and configure your system. For more advanced usage, consider exploring additional command-line resources and man pages.
