# Bandit Level 9

## Challenge Information
- **Level**: 9
- **Date Completed**: Sep 28, 2025
- **Time Spent**: 10 minutes
- **Connection**: `ssh bandit9@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Analysis
- The password is in the `data.txt` file which contains a bunch of non human-readable strings and other random characters.
- The password is preceded by several '=' characters.

## Thought Process
##### First Attempts:
1. Used `strings` in `data.txt` and it outputs a mess of characters but the password was easily identified, but I wanted a more efficient result.
## Solution
1. Used `strings` command with the pipe operator `|` and used `grep =` to search for the '=' characters.

### Commands Used:
```bash
# Step 1: [View directory contents]
ls

# Step 2: [Find printable characters in file | searched for '=' character in file]  
strings data.txt | grep =
```
### Next Level Password: 
```
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
## Screenshots
![[level-9-completed.png]]

## Key Learnings
##### New Commands:
- `strings` - Used to find and print sequences of printable characters in files.

## References & Resources
- https://overthewire.org/wargames/bandit/bandit10.html
