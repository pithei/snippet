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
9 | bandit.labs.overthewire.org | 2220 | bandit9 | UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR | [bandit 9](https://overthewire.org/wargames/bandit/bandit10.html) |
10 | bandit.labs.overthewire.org | 2220 | bandit10 | truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk | [bandit 10](https://overthewire.org/wargames/bandit/bandit11.html) |
11 | bandit.labs.overthewire.org | 2220 | bandit11 | IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR | [bandit 11](https://overthewire.org/wargames/bandit/bandit12.html) |
12 | bandit.labs.overthewire.org | 2220 | bandit12 | 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu | [bandit 12](https://overthewire.org/wargames/bandit/bandit13.html) |
13 | bandit.labs.overthewire.org | 2220 | bandit13 | 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL | [bandit 13](https://overthewire.org/wargames/bandit/bandit14.html) |
14 | bandit.labs.overthewire.org | 2220 | bandit14 | 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e | [bandit 14](https://overthewire.org/wargames/bandit/bandit15.html) |
15 | bandit.labs.overthewire.org | 2220 | bandit15 | BfMYroe26WYalil77FoDi9qh59eK5xNr | [bandit 15](https://overthewire.org/wargames/bandit/bandit16.html) |
16 | bandit.labs.overthewire.org | 2220 | bandit16 | cluFn7wTiGryunymYOu4RcffSxQluehd | [bandit 16](https://overthewire.org/wargames/bandit/bandit17.html) |
17 | localhost | 2220 | bandit17 | private key from tls service in lvl 16 | [bandit 17](https://overthewire.org/wargames/bandit/bandit18.html) |


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

## Level 8
```bash
bandit8@bandit:~$ cat data.txt | sort | uniq -c | grep -i "1 "
      1 UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
bandit8@bandit:~$
```

## Level 9
```bash
bandit9@bandit:~$ strings data.txt | grep -E '=='
========== the*2i"4
========== password
Z)========== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
bandit9@bandit:~$
```

## Level 10
```bash
bandit10@bandit:~$ cat data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
bandit10@bandit:~$
```

## Level 11
```bash
# https://en.wikipedia.org/wiki/ROT13
# Map upper case A-Z to N-ZA-M and lower case a-z to n-za-m
# $ tr 'A-Za-z' 'N-ZA-Mn-za-m' <<< "The Quick Brown Fox Jumps Over The Lazy Dog"
# Gur Dhvpx Oebja Sbk Whzcf Bire Gur Ynml Qbt,

bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
bandit11@bandit:~$
```

## Level 12
```bash
bandit12@bandit:~$ mkdir /tmp/pithei
bandit12@bandit:~$ cp data.txt /tmp/pithei
bandit12@bandit:~$ cd /tmp/pithei
bandit12@bandit:/tmp/pithei$ ls
data.txt
bandit12@bandit:/tmp/pithei$ xxd -r data.txt a.tar
bandit12@bandit:/tmp/pithei$ file a.tar
a.tar: gzip compressed data, was "data2.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
bandit12@bandit:/tmp/pithei$ mv a.tar a.gz
bandit12@bandit:/tmp/pithei$ gunzip a.gz

gzip: a.gz: decompression OK, trailing garbage ignored
bandit12@bandit:/tmp/pithei$ file a
a: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/pithei$ bunzip2 a
bunzip2: Can't guess original name for a -- using a.out
bandit12@bandit:/tmp/pithei$ file a.out
a.out: gzip compressed data, was "data4.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
bandit12@bandit:/tmp/pithei$ mv a.out a.gz
bandit12@bandit:/tmp/pithei$ gunzip a.gz
bandit12@bandit:/tmp/pithei$ file a
a: POSIX tar archive (GNU)
bandit12@bandit:/tmp/pithei$ tar xvpf a
data5.bin
bandit12@bandit:/tmp/pithei$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/pithei$ tar xvpf data5.bin
data6.bin
bandit12@bandit:/tmp/pithei$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/pithei$ bunzip2 data6.bin
bunzip2: Can't guess original name for data6.bin -- using data6.bin.out
bandit12@bandit:/tmp/pithei$ file  data6.bin.out
data6.bin.out: POSIX tar archive (GNU)
bandit12@bandit:/tmp/pithei$ tar xvpf data6.bin.out
data8.bin
bandit12@bandit:/tmp/pithei$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
bandit12@bandit:/tmp/pithei$ gunzip data8.bin
gzip: data8.bin: unknown suffix -- ignored
bandit12@bandit:/tmp/pithei$ mv data8.bin data8.gz
bandit12@bandit:/tmp/pithei$ gunzip data8.gz
bandit12@bandit:/tmp/pithei$ file data8
data8: ASCII text
bandit12@bandit:/tmp/pithei$ cat data8
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
bandit12@bandit:/tmp/pithei$
```

## Level 13
```bash
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost
#### < output ommited >
bandit14@bandit:~$ cat  /etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
bandit14@bandit:~$
```

## Level 14
```bash
bandit14@bandit:~$ echo 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e | nc localhost 30000
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr

bandit14@bandit:~$
```

## Level 15
```bash
bandit15@bandit:~$ echo "BfMYroe26WYalil77FoDi9qh59eK5xNr" | openssl s_client -connect localhost:30001 -ign_eof
#### < output ommited >
---
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd

closed
bandit15@bandit:~$
```

## Level 16
```bash
bandit16@bandit:~$ nmap -p  31000-32000 localhost

Starting Nmap 7.40 ( https://nmap.org ) at 2021-11-07 04:22 CET
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00027s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.09 seconds
bandit16@bandit:~$echo "cluFn7wTiGryunymYOu4RcffSxQluehd" | openssl s_client -connect localhost:31790 -ign_eof
#### < output ommited >
---
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$mkidr /tmp/pithei16
bandit16@bandit:~$cd /tmp/pithei16
cat >> private.key
## private key goes here
^D
bandit16@bandit:/tmp/pithei16$ chmod 600 private.key
bandit16@bandit:/tmp/pithei16$ ssh -i private.key bandit17@localhost
```

