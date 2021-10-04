# OverTheWire-Bandit-34level

![image](https://user-images.githubusercontent.com/62060867/135812681-c289c6e1-22cb-4c14-8af9-62663b98333c.png)

# Level 0

Use `ls`, we have `readme`.

`cat readme` we have password

```
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme 
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```
# Level 1

```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ file *
/dev/stdin: very short file (no magic)
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```
# Level 2

```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat *
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

```
# Level 3 

```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 May  7  2020 .
drwxr-xr-x 3 root    root    4096 May  7  2020 ..
-rw-r----- 1 bandit4 bandit3   33 May  7  2020 .hidden
bandit3@bandit:~/inhere$ cat .*
cat: .: Is a directory
cat: ..: Is a directory
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```
# Level 4

```
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```
# Level 5

```
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls -la
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

bandit5@bandit:~/inhere$ find -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```

# Level 6
```
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

```

# Level 7

```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep "millionth"
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV

```
# Level 8

```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

```
# Level 9

```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep ==
========== the*2i"4
========== password
Z)========== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

# Level 10

```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt 
VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==
bandit10@bandit:~$ cat data.txt  | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
# Level 11

```
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt 
Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh
bandit11@bandit:~$ cat data.txt | tr "A-Za-z" "N-ZA-Mn-za-m"
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```
