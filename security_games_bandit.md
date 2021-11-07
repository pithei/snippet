## Summary


level | URL | port | login | pass | Notes
---- | ---- | ---- | ---- | ---- | ----
0 | bandit.labs.overthewire.org | 2220 | bandit0 | bandit0 | [bandit 0](https://overthewire.org/wargames/bandit/bandit1.html) |
1 | bandit.labs.overthewire.org | 2220 | bandit1 | boJ9jbbUNNfktd78OOpsqOltutMc3MY1 | [bandit 1](https://overthewire.org/wargames/bandit/bandit2.html) |
2 | bandit.labs.overthewire.org | 2220 | bandit2 | CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9 | [bandit 2](https://overthewire.org/wargames/bandit/bandit3.html) |
3 | bandit.labs.overthewire.org | 2220 | bandit3 | UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK | [bandit 3](https://overthewire.org/wargames/bandit/bandit4.html) |
4 | bandit.labs.overthewire.org | 2220 | bandit4 | pIwrPrtPN36QITSp3EQaw936yaFoFgAB | [bandit 4](https://overthewire.org/wargames/bandit/bandit5.html) |


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
