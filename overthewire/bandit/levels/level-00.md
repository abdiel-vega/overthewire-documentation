# Bandit Level 0

## Challenge Information
- **Level**: 0
- **Date Completed**: Sep 25, 2025
- **Time Spent**: Like 1 minute
- **Connection**: `ssh bandit0@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Analysis
- There is a file with the password for level 1 somewhere in the home directory called **readme.**

## Solution
1. Viewed directory contents using `ls`.
2. Used `cat` to see `readme` file contents.

### Commands Used:
```bash
# Step 1: [View Directory Contents]
ls

# Step 2: [View file contents]  
cat readme
```
### Password: 
```
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```
## Screenshots
![[level-0-completion.png]]

## References & Resources
- https://overthewire.org/wargames/bandit/bandit1.html
