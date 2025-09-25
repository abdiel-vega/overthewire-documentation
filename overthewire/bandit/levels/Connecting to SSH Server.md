## Challenge Information
- **Level**: 0
- **Date Completed**: 24-Sep-2025
- **Time Spent**: Like 1 minute
- **Connection**: `ssh bandit0@bandit.labs.overthewire.org -p 2220`

## Level Goal
- The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.

## Introduction
```bash
Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
```


### Commands Used:
```bash
# Step 1: [Login to server using SSH]
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

### Password: 
```
bandit0
```

### Screenshots
![[lvl0-screenshot.png]]
## References & Resources
- https://overthewire.org/wargames/bandit/bandit0.html
