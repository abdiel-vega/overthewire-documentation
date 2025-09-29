# Bandit Level 14

## Challenge Information
- **Level**: 14
- **Date Completed**: Sep 29, 2025
- **Time Spent**: 10 minutes
- **Connection**: `ssh bandit14@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Analysis
- I already have the password for this level which I found by following the path specified on the previous level.
- I need to submit the password on port 30000 on localhost.

## Solution
1. Used `cat /etc/bandit_pass/bandit14` to view password file and copy it.
2. Used Netcat to connect to localhost 30000 and entered the current level password.

### Commands Used:
```bash
# Step 1: [View password file contents]
cat /etc/bandit_pass/bandit14

# Step 2: [Connected to localhost 30000 and entered password]  
nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
### Next Level Password: 
```
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
## Screenshots
![[level-14-completed 1.png]]

## Key Learnings
##### New Commands/Concepts:
- Netcat can be used to connect to a localhost TCP or UDP network connection through a port number.

## References & Resources
- https://overthewire.org/wargames/bandit/bandit15.html
- https://computer.howstuffworks.com/web-server8.htm
- https://en.wikipedia.org/wiki/Localhost
- https://en.wikipedia.org/wiki/Port_(computer_networking)
