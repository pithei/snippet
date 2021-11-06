## not clear, TBD list for pen testing
Key | Value
---- | ----
Target level | Generic understanding
Learning Sources | JPT > WAPT > OSCP. CPPT <br /> https://www.sans.org/cyber-security-skills-roadmap/ <br />https://elearnsecurity.com/product/ejpt-certification/ <br /> https://github.com/sundowndev/hacker-roadmap <br /> https://onlinedegrees.sandiego.edu/top-cyber-security-blogs-websites/ <br />
Skill list | git <br /> python <br /> linux <br /> networking 
Task list | YAML device Inventory <br /> Base config verification with ansible <br />
Daily time slot | time
Tools to obtain | Accounts (email, cisco devnet, github) <br /> [Ubuntu desktop VM](https://github.com/pithei/py100/blob/master/6_cisco_devnet/001_ubuntu_prep.txt) <br /> Git <br /> Postman <br /> Python <br /> Docker <br /> VSCode <br />


## Tips
- Eliminate any barrier
- Learn enough to self correct
- choose a project
- create fast feedback oops
- quantity over quality
- practice minimum 20 hours
- spaced repetition

## Notes

```bash
   # comment
   echo "hi"
//
```

https://www.amazon.com/Blue-Team-Field-Manual-BTFM/dp/154101636X
https://www.amazon.com/Applied-Network-Security-Monitoring-Collection/dp/0124172083
https://www.amazon.com/Rtfm-Red-Team-Field-Manual/dp/1494295504![image](https://user-images.githubusercontent.com/73688531/140619808-73ba8f4d-be81-45e6-b711-8672f13a625f.png)


https://picoctf.com/external

https://ctflearn.com/1/scoreboard/0
https://ctf101.org/
https://trailofbits.github.io/ctf/intro/
https://learningnetwork.cisco.com/s/devnet-associate-exam-topics


https://portswigger.net/web-security/sql-injection![image](https://user-images.githubusercontent.com/73688531/140619014-0b892241-ff05-4a98-acb8-89b0c3a153d8.png)


#wargames

for a in {0..9}; do for b in {0..9}; do for c in {0..9}; do for d in {0..9}; do echo $a$b$c$d; echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $a$b$c$d" | nc localhost 30002 -w 1 2>&1 >> output.log &; done; done; done; done



for a in {0..9}; do for b in {0..9}; do for c in {0..9}; do for d in {0..9}; do echo "echo 'UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $a$b$c$d' | nc localhost 30002 -w 1 2>&1 >> /var/spool/bandit24/servetoo/log/$a$b$c$d.txt &" >> thelist.txt; done; done; done; done




IFS=$'\n';for line in `cat thelist.txt`; do command ${line} > ${line}; done
IFS=$'\n';for line in `cat thelist.txt`; do command ${line}; done


/bin/bash << EOF
big ugly commands
lots of them
EOF


ssh bandit26@localhost -i bandit26.sshkey /bin/bash << EOF
cat text.txt
EOF![image](https://user-images.githubusercontent.com/73688531/140619018-301ba479-fb90-4b67-a3b4-f6bf96eca0da.png)

