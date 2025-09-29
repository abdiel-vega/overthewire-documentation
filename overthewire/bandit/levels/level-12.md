# Bandit Level 12

## Challenge Information
- **Level**: 12
- **Date Completed**: Sep 28, 2025
- **Time Spent**: 40 minutes
- **Connection**: `ssh bandit12@bandit.labs.overthewire.org -p 2220`

## Level Goal

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Analysis
- The password is in the `data.txt` file which is a hexdump of a file that has been repeatedly compressed.
- A lot of converting is needed.

## Thought Process
##### First Attempts:
1. Followed instructions and set a temporary directory, copy and pasted `data.txt` file into new directory.
2. Searched in the internet for ways to uncompress a hexdump file.
## Solution
1. Used `xxd` command with the revert flag `-r` to decompress the hexdump file and sent the data over to a new `data2.txt` file.
2. Used `file data2.txt` to see file type. File is using `gzip` for compression.
3. Used `gunzip -c data2.txt > data3.txt` to decompress `data2.txt` into `data3.txt` file
4. Used `file data3.txt` to see file type. File is using `bzip2` for compression.
5. Repeated file type identification and decompressing until password appeared.

### Commands Used:
```bash
# Step 1: [Make temporary directory to work on]
mktemp -d

# Step 2: [Revert hexdump file | output into data.bin file]  
xxd -r > data2.txt

# Step 3: [Check file type to determine how to decompress next]
file data2.txt

# Step 4: [Decompress to data4.txt]
bunzip2 -c data3.txt > data4.txt

# Step 5: [Check file type]
file data4.txt

# Step 6: [Decompress to data5.txt]
gunzip -c data4.txt > data5.txt

# Step 7: [Check file type]
file data5.txt

# Step 8: [Decompress file]
tar -xf data5.txt

# ... Keep repeating process until file type is ASCII text

# Step 9: [View file contents]
cat data9.txt
```
### Next Level Password: 
```
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
## Screenshots
![[level-12-temp-dir.png]]
![[level12-completed.png]]
## Key Learnings
##### New Commands/Concepts:
- A lot of compression methods in Linux. These compression methods can be used together. Usual compression methods in Linux include:
	- `gzip`
	- `bzip2`
	- `tar`

## References & Resources
- https://overthewire.org/wargames/bandit/bandit13.html
- https://en.wikipedia.org/wiki/Hex_dump