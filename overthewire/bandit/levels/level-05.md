# Bandit Level 5

## Challenge Information
- **Level**: 5
- **Date Completed**: Sep 25, 2025
- **Time Spent**: 15 minutes
- **Connection**: `ssh bandit5@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable

## Analysis
- The password file is somewhere in `inhere/` directory which has 20 more sub directories ranging from `maybehere00` through `maybehere19`.
- Each `maybehere` sub-directory have multiple files.
- The password file is 1033 bytes in size.
- Need to try and search which file is 1033 bytes in size in all the files within the `maybehere` sub-directories.

## Solution
1. In the `inhere/` directory
2. Used `find -size 1033c` (c = bytes)
recursively 
### Commands Used:
```bash
# Step 1: [Change to inhere/ directory]
cd inhere/

# Step 2: [List all directories and files recursively]  
ls -R

# Step 3: [Find file with size of 1033 bytes]  
find -size 1033c
```
### Password: 
```
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
## Screenshots
![[level-5-completed.png]]

## Key Learnings
##### New Commands/Concepts:
- `find -size n[cwbkMG]`
- File uses less than, more than or exactly n units of space, rounding up. The following suffixes can be used:
```
'b'    for 512-byte blocks (this is the default if no suffix is used)
'c'    for bytes
'w'    for two-byte words
'k'    for kibibytes (KiB, units of 1024 bytes)
'M'    for mebibytes (MiB, units of 1024 * 1024 = 1048576 bytes)
'G'    for gibibytes (GiB, units of 1024 * 1024 * 1024 = 1073741824 bytes)
```

## References & Resources
- https://overthewire.org/wargames/bandit/bandit6.html
- https://manpages.ubuntu.com/manpages/noble/man1/find.1.html