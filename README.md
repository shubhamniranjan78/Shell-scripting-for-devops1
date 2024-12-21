# Linux Shell Script for User Management and Backup

Hey there! This is a simple but practical shell script I've developed to help automate some common Linux system administration tasks, specifically:

*   Managing user accounts (adding, deleting, modifying).
*   Managing groups.
*   Creating backups of directories.

I built this project to consolidate my understanding of Linux, Bash scripting, and version control with Git. I hope you find it useful, and if you have any ideas for improvements, I'm all ears!

## Overview

The primary goal of this script is to provide a single tool that allows efficient management of user accounts, groups and reliable backups of specified directories. It's designed to be flexible enough for use on different Linux distributions.

### Key Features

*   **User Management:** Allows you to add new users, delete existing users, and modify user passwords.
*   **Group Management:**  Allows you to create new groups.
*   **Automated Backups:**  Creates compressed archive files of directories.
*   **Clear CLI:** The script provides a user-friendly command-line interface with clear instructions using the `getopts` command.
* **User Input Validation:** Basic input validation to make sure users do not pass in null inputs.

## Requirements

Before getting started, you'll need the following:

1.  **Linux OS:** Any distribution (Ubuntu, Fedora, etc.) will work.
2.  **Bash Shell:** The default on most Linux systems.
3.  **Git and GitHub:** For version control (clone the repo).
4.  **Text Editor:** For viewing or modifying the script (like Vim, Nano, or VS Code).

## Getting Started

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/LondheShubham153/Shell-Scripting-For-DevOps
    cd Shell-Scripting-For-DevOps
    ```

2.  **Make the Script Executable:**
    ```bash
    chmod +x your_script_name.sh
    ```

3.  **Run the script as a Root/with Sudo:**
    ```bash
    sudo ./your_script_name.sh <options>
    ```

## Usage

The script uses command-line options:

*   `-u <username>`: Add a new user.
*   `-d <username>`: Delete a user.
*   `-m <username>`: Change password for a user.
*   `-g <groupname>`: Create a new group.
*   `-b <directory>`: Back up a directory.
*   `-h`: Display help message.

### Examples

*   To create a new user called `john`
    ```bash
    sudo ./your_script_name.sh -u john
    ```
*  To delete a user called `john`
    ```bash
    sudo ./your_script_name.sh -d john
    ```
*  To create a new group called `developers`
   ```bash
   sudo ./your_script_name.sh -g developers
    ```
*   To back up a directory called `/home/testfolder`:
   ```bash
    sudo ./your_script_name.sh -b /home/testfolder
Use code with caution.
Markdown
To change password of a user called john

sudo ./your_script_name.sh -m john
Use code with caution.
Bash
To display help message:

sudo ./your_script_name.sh -h
Use code with caution.
Bash
Implementation Details
The script uses core Linux commands like useradd, userdel, usermod, groupadd, tar, etc.

getopts handles command-line option parsing.

Error handling is basic but present (it could be further improved!).

The backup uses tar to compress and archive the specified directory.

Security is a key consideration, making sure commands needing root permission are run via sudo.

What I've Learned
The power and flexibility of shell scripting.

The importance of clear command-line interfaces.

Better understanding of Linux user management commands.

The crucial role of version control using Git.

Improvements
There are plenty of ways to improve this script. Here are a few ideas:

Add more robust error handling.

Add more options for managing groups.

Support different backup strategies.

Implement more validation checks for user input.

Contributing
Feel free to fork this repository and submit pull requests! If you have any suggestions or find any bugs, please let me know. I'm always open to learning and improving.

Happy scripting!
