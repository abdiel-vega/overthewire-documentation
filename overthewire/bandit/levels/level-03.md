# Bandit Level 3

## Challenge Information
- **Level**: 3
- **Date Completed**: Sep 25, 2025
- **Time Spent**: 5 minutes
- **Connection**: `ssh bandit3@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in a hidden file in the **inhere** directory.

## Analysis
- The password for the next level is stored in a file in the `/inhere` directory

## Solution
1. Used `ls` to view directory contents and `cd inhere/` to travel to directory/
2. Used `ls -la` to view all directory contents and found the password file as a hidden file named `...Hiding-From-You`

### Commands Used:
```bash
# Step 1: [View current directory and go to inhere/ directory]
ls
cd inhere/

# Step 2: [View all contents of current directory]  
ls -la

# Step 3: [View hidden file contents]
cat ...Hiding-From-You
```
### Next Level Password: 
```
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
## Screenshots
![[level-3-completed.png]]

## References & Resources
- https://overthewire.org/wargames/bandit/bandit4.html