# Bandit Level 10

## Challenge Information
- **Level**: 10
- **Date Completed**: Sep 28, 2025
- **Time Spent**: 10 minutes
- **Connection**: `ssh bandit10@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.

## Analysis
- The password is in the `data.txt` file which contains base64 encoded data.
- `cat` will not suffice.

## Solution
1. Used `base64 -d` command in conjunction with `cat` command to decode and view file contents.

### Commands Used:
```bash
# Step 1: [View directory contents]
ls

# Step 2: [View file contents | decode file contents]  
cat data.txt | base64 -d
```
### Next Level Password: 
```
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
## Screenshots
![[level-10-completed.png]]

## Key Learnings
##### New Commands/Concepts:
- The `base64` command on Linux encodes and decodes data using the Base64 standard. This process converts binary data into a text-only format

## References & Resources
- https://overthewire.org/wargames/bandit/bandit11.html
