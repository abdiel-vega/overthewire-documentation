# Bandit Level 2

## Challenge Information
- **Level**: 2
- **Date Completed**: Sep 25, 2025
- **Time Spent**: 10 minutes
- **Connection**: `ssh bandit2@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory.

## Analysis
- Password for next level is in file: `--spaces in this filename--`.
- Can't use regular old `cat` to view file contents because of spaces in the filename, called a continuous file.

## Thought Process
##### First Attempts:
1. Used `ls -la` to view directory contents and find out which type of file is `--spaces in this filename--`.
2. Tried to use `cat "--spaces in this filename--"` and `cat --spaces\ in\ this\ filename--`

## Solution
1. Went into `cat --help` and in the page it read: `With no FILE, or when FILE is -, read standard input.`
2. Used `cat < "--spaces in this filename--"` to view file contents through input redirection.

### Commands Used:
```bash
# Step 1: [View Directory Contents]
ls -la 

# Step 2: [View continuous file contents]  
cat < "--spaces in this filename--"
```
### Next Level Password: 
```
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```
## Screenshots
![[level-2-completed.png]]

## Key Learnings
##### New Concept:
- Use input redirection `<` to view continuous file contents (files with spaces)

## References & Resources
- https://overthewire.org/wargames/bandit/bandit3.html
