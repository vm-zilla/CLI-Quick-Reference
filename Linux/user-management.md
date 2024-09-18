**User identification commands**

| Command | Description                |
|---------|----------------------------|
| who     | Lists all logged-in users  |
| finger  | Logged in user information |
| id      | Get user and group ID      |



**User account management commands**

| Command | Description               |
|---------|---------------------------|
| useradd | Create a new user account |
| userdel | Delete an existing user   |
| usermod | Modify user account       |
| passwd  | Manage use passwords      |



**Group management**

| Command  | Description             |
|----------|-------------------------|
| groupadd | Creates new groups      |
| groupdel | Delete a group          |
| groupmod | Modify group properties |


## Sample Usage

| useradd vmzilla  | This command will add a new user named vmzilla |
|------------------|------------------------------------------------|
| password vmzilla | This command will help set password for user |


Once a new user is created, its entry is automatically added to the ‘/etc/passwd‘ file. This file is used to store the user’s information, and the entry should be.

Linux# cat /etc/passwd | grep vmzilla
vmzilla:x:1000:1000::/home/vmzilla:/bin/sh

The above entry contains a set of seven colon-separated fields, each field having its own meaning.

Let’s see what these fields are:

1. Username – The user login name is used to log into the system. It should be between 1 and 32 characters long.
2. Password – The user password (or 'x' character) is stored in the ‘/etc/shadow‘ file in an encrypted format.
3. User ID (UID) – Every user must have a User ID (UID), which stands for User Identification Number. By default, UID 0 is reserved for the root user, and UIDs ranging from 1 to 99 are reserved for other predefined accounts. Additionally, UIDs ranging from 100 to 999 are reserved for system accounts and groups.
4. Group ID (GID) – The primary Group ID (GID), which stands for Group Identification Number, is stored in the ‘/etc/group‘ file.
5. User Info – This field is optional and allows you to define extra information about the user, such as the user’s full name. This information can be filled in using the finger command.
6. Home Directory – The absolute location of the user’s home directory.
7. Shell – The absolute location of a user’s shell i.e. /bin/bash.

## Sample Usage

| useradd -d /data/projects vmzilla          | Specify user home dir at the time of user creation |
| useradd -u 1002 vmzilla                    | Create user with specific user ID                  |
| useradd -u 1005 -g admin vmzilla           | Create user with specific group                    |
| usermod -a -G group1,group2,group3 vmzilla | Adding user to multiple group                      |
| useradd -M vmzilla                         | Adding user without home dir                       |
| useradd -e 2024-08-27 vmzilla              | Adding user with expiry                            |
| chage -l vmzilla                           | Verify the account and password aging information  |
| useradd -e 2014-04-27 -f 45 vmzilla        | Set password expiry usin -f                        |
