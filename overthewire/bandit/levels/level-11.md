# Bandit Level 11

## Challenge Information
- **Level**: 11
- **Date Completed**: Sep 28, 2025
- **Time Spent**: 15 minutes
- **Connection**: `ssh bandit11@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

## Analysis
- The password is in `data.txt`, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.
- Researched on internet and found this is called **ROT13** cipher. 

## Solution
1. Used `tr` command and provided the alphabet as the first set and the ROT13-shifted alphabet as the second.

### Commands Used:
```bash
# Step 1: [View directory contents]
ls

# Step 2: [View file contents | decode ROT13 message]  
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-n'
```
### Next Level Password: 
```
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
## Screenshots
![[level-11-completed.png]]

## Key Learnings
##### New Commands/Concepts:
- `tr` for translating characters from standard input.
- **ROT13** is a simple letter substitution cipher that replaces a letter with the 13th letter after it in the Latin alphabet.
- Can use `tr` to decode **ROT13** cipher in Linux terminal by using:
	- `tr 'A-Za-z' 'N-ZA-Mn-za-n'`

## References & Resources
- https://overthewire.org/wargames/bandit/bandit12.html
- https://en.wikipedia.org/wiki/ROT13