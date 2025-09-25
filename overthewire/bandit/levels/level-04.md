# Bandit Level 4

## Challenge Information
- **Level**: 4
- **Date Completed**: Sep 25, 2025
- **Time Spent**: 10 minutes
- **Connection**: `ssh bandit4@bandit.labs.overthewire.org -p 2220`

## Level Goal
- The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Analysis
- The password for the next level is stored in a file in the `/inhere` directory
- There are 10 total files ranging from `-file00` to `-file09`. 
- One of them probably contains the password.

## Thought Process
- Searched for ways to view contents of multiple files in a directory.
- Learned about wildcard `*` character
## Solution
1. Used `less` to see file contents one by one. Combined with `./*` which tells it to use the command in the current `inhere/` directory, and the wildcard `*` tells the command to take every file inside the directory.
2. Found password in `-file08`

### Commands Used:
```bash
# Step 1: [View current directory and go to inhere/ directory]
ls
cd inhere/

# Step 2: [View all contents of current directory]  
ls -la

# Step 3: [View file contents one by one]
less ./*
```
### Password: 
```
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
## Screenshots
![[level-4-completed.png]]
![[passwd-in-file08.png]]

## Key Learnings
##### New Commands/Concepts:
- Use `./` for current directory
- Use wildcard `*` character for any file type in a directory
- Use `less` command to view multiple file contents one by one

## References & Resources
- https://overthewire.org/wargames/bandit/bandit5.html
