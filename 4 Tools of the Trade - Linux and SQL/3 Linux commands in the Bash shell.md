## Basic commands

- `pwd`: Print Working Directory (e.g. current)
- `ls`: LiSt files and directories in current directory
- `cd`: Change Directory
- `cat`: conCATenate file contents onto screen.
- `head`: Display first 10 lines of file.
- `tail`: Display last 10 lines of file.
- `less`: Display file contents in "pages".

## Standard FHS directories

- `/home/x` = `~`: Each user has a home directory.
- `/bin`: BINary files and executables.
- `/etc`: System config files.
- `/tmp`: Temporary files.
- `/mnt`: Mounted media such as USB / hard drives.

## Managing content

### grep

- Searches a specified file, returns all lines containing that string.
- E.g. `grep mytext myfile.txt`.

### Piping

- Sends stdout from one command to stdin of another.
- Represented with `|`.
- E.g. `ls /home/username/reports | grep users`.

### find

- Command used to find files & directories that meet criteria.
- E.g. `find /reports -name "users*"` finds all files starting with "users". `-iname` is case-insensitive version.
- E.g. `find /reports -mtime -1` finds all files last modified under a day ago, whilst `+1` would find over a day ago. `mmin` is the same, but for minutes.

### > & >>

Similar to piping, angle brackets can send output into a file. `>` overwrites, `>>` adds to/appends.

### Creating and modifying directories & files

- `mkdir`: MaKe DIRectory
- `rmdir`: ReMove DIRectory
- `touch`: Make file
- `rm`: ReMove file
- `mv`: MoVe file (can also rename)
- `cp`: CoPy file

### File editors

`nano` is a popular beginner-friendly editor:

- `nano myfile.txt`
- Ctrl-O save.
- Ctrl-X exit.

## File Permissions & Ownership

- 3 types of permission in Linux:
  - Read: read file contents or read files in directory 
  - Write: modification of file contents or creation of new files in directory
  - Execute: execute file or enter directory and access files
    
- 3 types of owners:
  - User
  - Group
  - Other
  
- Representation of file permissions through 10-character string: `drwxrwxrwx`
  - `d`irectory
  - `r`eadable
  - `w`ritable,
  - e`x`ecutable by all.
  - `-` for regular file or whenever user lacks permission.
  - "World-writable file" = User, group, and other can all write to a file (security risk).

## Checking Permissions through Options

Modify command behaviour eg. to check permissions
- `ls -l` displays permissions.
- `ls -a` displays hidden files.
- `ls -la` displays hidden files and permissions.
  
### Change Permissions

- chmod: `ch`ange `mod`e: Change perms on files & directories.
- E.g. Symbolic mode: `chmod g+w,o-r access.txt` = Modify access.txt, `g`roup add `w`rite, `o`ther remove `r`ead.
  - Adds: chmod u+rwx,g+rwx,o+rwx login_sessions.txt
  - Assigns: chmod u=r,g=r,o=r login_sessions.txt
  - Removes: chmod u-rwx,g-rwx,o-rwx login_sessions.txt
- `chown` also exists, to change who owns a file.

### Users

- "root user" or "superuser": can read/write/delete any file & run any program.
- A superuser can add new users.
- Problems logging in as s/u:
  - Security risk (should have log ins disabled)
  - Irreversib;e mistakes
  - Accountability (sudo command is solution)
- `sudo` (super-user-do): Temporarily run as superuser, only available to users in the "sudoers file".
- `useradd`: Add a user, e.g. `sudo useradd myusername`. For groups:
  - `-g` adds to primary group e.g. `sudo useradd -g security fgarcia` 
  - `-G` adds to secondary group(s) e.g. `sudo useradd -G finance,admin fgarcia `
- `userdel`: Delete a user, e.g. `sudo userdel myusername`.
  - Follow up with: `sudo groupdel fgarcia` (When you create a new user, a group with the same name as the user is automatically created) 
  -  `-r`: deletes user and all files in their home directory e.g. `sudo userdel -r fgarcia`
- `usermod`: Modify a user, e.g.
  - `-g`: Modify default group membership with `sudo usermod -g mygroup myusername`
  -  `-a -G`: add user to supplemental group sudo `usermod -a -G marketing fgarcia` 
  - `-d`: change user's home directory
  - `-l`: Can change login name
  - `-L`: Can lock account
- `chown`: change file/directory owner e.g. `sudo chown john access.txt`, or for group owners `sudo chown :security access.txt`


## Looking up info

- `man`: Displays full info on how commands work, comes from `man`ual.
- `whatis`: Provides a one-line summary of a command.
- `apropos`: Search man docs by a term, can also call with `-a` for multiple terms eg. `apropos -a change password`

## Feedback

Lab is again excellent, requiring applying knowledge instead of explicitly stating what needs to be done. It's great that Reddit / Unix & Linux Stack Exchange are mentioned / linked, many courses skip the "real world" information finding.
