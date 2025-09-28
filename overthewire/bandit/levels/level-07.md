# Bandit Level 7

## Challenge Information
- **Level**: 7
- **Date Completed**: Sep 28, 2025
- **Time Spent**: 5 minutes
- **Connection**: `ssh bandit7@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in the file **data.txt** next to the word **millionth**.

## Analysis
- The password file is in a file named `data.txt` next to the word **millionth**.
- There is only the one file in the server, but it contains too much text to read.

## Solution
1. Used `grep` command to search for the word **millionth**.

### Commands Used:
```bash
# Step 1: [View all contents of current directory]
ls -la

# Step 2: [Searched for word 'millionth' in data.txt]  
grep millionth data.txt
```
### Next Level Password: 
```
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
## Screenshots
![[level-7-completed.png]]

## References & Resources
- https://overthewire.org/wargames/bandit/bandit8.html
