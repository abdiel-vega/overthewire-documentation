# Bandit Level 6

## Challenge Information
- **Level**: 6
- **Date Completed**: Sep 28, 2025
- **Time Spent**: 15 minutes
- **Connection**: `ssh bandit6@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Analysis
- I need to find the password file somewhere on the server.
- The file is owned by `bandit7` user and `bandit6` group.
- The file is 33 bytes in size.

## Thought Process
##### First Attempts:
1. Used `ls -la` but no files appear.
2. Used `find / -user bandit7 -group bandit6 -size 33c` to locate the file in the server but outputted a lot of filed with denied access.
## Solution
1. Used `find / -user bandit7 -group bandit6 -size 33c 2>/dev/null` to redirect any denied directories and files to the `/dev/null` file to see a clean output.

### Commands Used:
```bash
# Step 1: [View all contents of current directory]
ls -la

# Step 2: [Find specific file owned by bandit7 user and bandit6 group of 33 bytes, while redirecting any denied access files/directories to black hole]
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```
### Next Level Password: 
```
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```
## Screenshots
![[level-6-completed.png]]

## Key Learnings
##### New Commands/Concepts:
- Add `2>/dev/null` to the end of a command to redirect all errors and permission denial output to the trash basically.

## References & Resources
- https://overthewire.org/wargames/bandit/bandit7.html
