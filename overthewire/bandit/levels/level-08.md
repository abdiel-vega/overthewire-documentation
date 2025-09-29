# Bandit Level 8

## Challenge Information
- **Level**: 8
- **Date Completed**: Sep 28, 2025
- **Time Spent**: 20 minutes
- **Connection**: `ssh bandit8@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once.

## Analysis
- The password is in the `data.txt` file and is the only line of text that occurs only once.
- The text file is full of random characters.
- `uniq` command removes duplicate lines from a file but ignores duplicate lines if they are not adjacent.

## Thought Process
##### First Attempts:
1. Tried to do a number of combinations of the `sort`and `uniq`command with different flags.
## Solution
1. Performed `sort` command to sort all duplicate lines adjacent to each other.
2. Used the pipe operator `|` to perform a `uniq -c` command after the sort to show how many times each line appears.
3. The output was a bunch of different lines with 10 occurrences each, except for one which is the password.

### Commands Used:
```bash
# Step 1: [View contents of current directory]
ls

# Step 2: [View file contents | sort file contents | remove duplicate lines and view each duplicate lines count]  
cat data.txt | sort | uniq -c
```
### Next Level Password: 
```
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```
## Screenshots
![[level-8-completed.png]]

## Key Learnings
##### New Commands/Concepts:
- `cat [file] | sort | uniq -c` for sorting text in a file and finding unique lines of text in a file.

## References & Resources
- https://overthewire.org/wargames/bandit/bandit9.html
