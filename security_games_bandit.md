## Summary


level | URL | port | login | pass | Notes
---- | ---- | ---- | ---- | ---- | ----
0 | bandit.labs.overthewire.org | 2220 | bandit0 | bandit0 | [bandit 0](https://overthewire.org/wargames/bandit/bandit1.html) |
1 | bandit.labs.overthewire.org | 2220 | bandit1 | boJ9jbbUNNfktd78OOpsqOltutMc3MY1 | [bandit 1](https://overthewire.org/wargames/bandit/bandit2.html) |
2 | bandit.labs.overthewire.org | 2220 | bandit2 | CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9 | [bandit 2](https://overthewire.org/wargames/bandit/bandit3.html) |
3 | bandit.labs.overthewire.org | 2220 | bandit3 | UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK | [bandit 3](https://overthewire.org/wargames/bandit/bandit4.html) |
4 | bandit.labs.overthewire.org | 2220 | bandit4 | pIwrPrtPN36QITSp3EQaw936yaFoFgAB | [bandit 4](https://overthewire.org/wargames/bandit/bandit5.html) |
5 | bandit.labs.overthewire.org | 2220 | bandit5 | koReBOKuIDDepwhWk7jZC0RTdopnAYKh | [bandit 5](https://overthewire.org/wargames/bandit/bandit6.html) |
6 | bandit.labs.overthewire.org | 2220 | bandit6 | DXjZPULLxYr17uwoI01bNLQbtFemEgo7 | [bandit 6](https://overthewire.org/wargames/bandit/bandit7.html) |
7 | bandit.labs.overthewire.org | 2220 | bandit7 | HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs | [bandit 7](https://overthewire.org/wargames/bandit/bandit8.html) |
8 | bandit.labs.overthewire.org | 2220 | bandit8 | cvX2JJa4CFALtqS87jk27qwqGhBM9plV | [bandit 8](https://overthewire.org/wargames/bandit/bandit9.html) |

## Level 0

```bash
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
bandit0@bandit:~$
```

## Level 1
```bash
# https://www.golinuxcloud.com/overview-bash-dashed-filename-directory-linux/
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
bandit1@bandit:~$
```

## Level 2
```bash
bandit2@bandit:~$ cat spaces\ in\ this\ filename
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
bandit2@bandit:~$
```

## Level 3
```bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -al
total 12
drwxr-xr-x 2 root    root    4096 May  7  2020 .
drwxr-xr-x 3 root    root    4096 May  7  2020 ..
-rw-r----- 1 bandit4 bandit3   33 May  7  2020 .hidden
bandit3@bandit:~/inhere$ cat .hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
bandit3@bandit:~/inhere$
```

## Level 4 
```bash
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ find inhere/ -type f -exec file {} \;
inhere/-file01: data
inhere/-file00: data
inhere/-file06: data
inhere/-file03: data
inhere/-file05: data
inhere/-file08: data
inhere/-file04: data
inhere/-file07: ASCII text
inhere/-file02: data
inhere/-file09: data
bandit4@bandit:~$
bandit4@bandit:~$ cat inhere/-file07
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
bandit4@bandit:~$
```
## Level 5
```bash
bandit5@bandit:~$ ls inhere/ -al
total 88
drwxr-x--- 22 root bandit5 4096 May  7  2020 .
drwxr-xr-x  3 root root    4096 May  7  2020 ..
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere00
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere01
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere02
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere03
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere04
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere05
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere06
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere07
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere08
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere09
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere10
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere11
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere12
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere13
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere14
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere15
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere16
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere17
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere18
drwxr-x---  2 root bandit5 4096 May  7  2020 maybehere19
bandit5@bandit:~$ find inhere/ | wc -l
201
bandit5@bandit:~$ find ./ -type f -size 1033c
./inhere/maybehere07/.file2
bandit5@bandit:~$ cat ./inhere/maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        bandit5@bandit:~$
```

## Level 6
```bash
bandit6@bandit:~$ ls -al
total 20
drwxr-xr-x  2 root root 4096 May  7  2020 .
drwxr-xr-x 41 root root 4096 May  7  2020 ..
-rw-r--r--  1 root root  220 May 15  2017 .bash_logout
-rw-r--r--  1 root root 3526 May 15  2017 .bashrc
-rw-r--r--  1 root root  675 May 15  2017 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
bandit6@bandit:~$
```

## Level 7
```bash
andit7@bandit:~$ grep millionth data.txt
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV
bandit7@bandit:~$
```
