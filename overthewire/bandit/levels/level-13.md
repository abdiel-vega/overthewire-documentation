# Bandit Level 13

## Challenge Information
- **Level**: 13
- **Date Completed**: Sep 29, 2025
- **Time Spent**: 10 minutes
- **Connection**: `ssh bandit13@bandit.labs.overthewire.org -p 2220`

## Level 13 Goal

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on.

## Analysis
### What I Know:
- The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**.
- There is a file named `sshkey.private` in the level directory.
- We need to connect to level 14 from this current level using the SSH key provided in the `sshkey.private` file.

## Solution
1. Used `ssh bandit14@bandit.labs.overthewire.org -p 2220 -i sshkey.private` command to connect to bandit level 14 using the provided ssh key.
2. Since we are connected to level 13 and entering level 14 we can use the `-i` flag to identify the `sshkey.private` file.
3. Connected to level 14 and used `cat /etc/bandit_pass/bandit14` to view password file.

### Commands Used:
```bash
# Step 1: [View directory contents]
ls

# Step 2: [Connect to level 14 through level 13]  
ssh bandit14@bandit.labs.overthewire.org -p 2220 -i sshkey.private

# Step 3: [View file contents from /etc/bandit_pass/bandit14]
cat /etc/bandit_pass/bandit14
```
### Next Level Password: 
```
N/A - Connected to bandit14 with a ssh key available in bandit13
```
## Screenshots
![[level13-sshkey.png]]
![[overthewire/bandit/assets/screenshots/level-14-completed.png]]
## Key Learnings
##### New Commands/Concepts:
- Can use an `-i` flag when establishing an SSH connection to redirect to a SSH key file.

## References & Resources
- https://overthewire.org/wargames/bandit/bandit14.html
