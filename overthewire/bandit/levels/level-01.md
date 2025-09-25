# Bandit Level 1

## Challenge Information
- **Level**: 1
- **Date Completed**: Sep 25, 2025
- **Time Spent**: 5 minutes
- **Connection**: `ssh bandit1@bandit.labs.overthewire.org -p 2220`

## Level Goal
- The password for the next level is stored in a file called **-** located in the home directory.

## Analysis
- There is a file with the password for level 2 somewhere in the home directory called **-**.

## Thought Process
##### First Attempts:
1. Used `ls` to view directory contents and found `-` file.
2. Tried to use `ls` and `nano` to view file contents but couldn't.
3. Found in a post on StackOverflow and found the following comment from user Prithvi Raj on this exact problem.
> "This type of approach has a lot of misunderstanding because using **-** as an argument refers to **STDIN/STDOUT** i.e **dev/stdin** or **dev/stdout** .So if you want to open this type of file you have to specify the full location of the file such as `./-` .For eg. , if you want to see what is in that file use `cat ./-`"

## Solution
1. Viewed directory contents using `ls`
2. Used `cat` to see `./-` file contents

### Commands Used:
```bash
# Step 1: [View Directory Contents]
ls

# Step 2: [View file contents]  
cat ./-
```
### Password: 
```
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
## Screenshots
![[level-1-completed.png]]

## Key Learnings
##### New Concept:
- Use `./` to specify full location of special character files .

## References & Resources
- https://overthewire.org/wargames/bandit/bandit2.html
- https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal
- https://linux.die.net/abs-guide/special-chars.html