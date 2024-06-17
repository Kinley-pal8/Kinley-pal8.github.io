---
Title: Journal 4
categories: [SWS101, CTF Journal]
tags: [SWS101]
---

### Topic : Bounty Hacker - TryHackMe Walkthrough 

#### Introduction:
In this journal, I’ll be recounting the activity involving the completion of the Bounty Hacker CTF in TryHackMe. To me it is relevant to keep track and record my progress as well as the things I learn from the challenges of cyber security. In doing so, I would like to achieve not only the improvement of understanding of the subject matter, but also contribute to the better comprehension of the knowledge for those, who is in the same process as me.

#### Walkthrough:

The Bounty Hacker CTF featured some of the most fascinating tasks that identified my capability to port scan, gain access to FTP services, SSH brute-forcing, and privilege escalation. I began by performing a port scan using nmap, which revealed three open ports: Port no 21 for FTP , 22 for SSH and 80 for HTTP. 

Upon further investigation, I discovered that anonymous access was available on the FTP service, and I found two interesting text files: In the case of an individual knowledge worker whose main job is to perform a single task, what might not be good for one type of business could actually be optimal for the other type of business depending on the nature of the task. txt and locks. txt.
Using the locks. I was also able to login to the machine with the user lin through SSH using the password fetched from the lin. txt file where I used hydra to brute force the password. With the obtained credential, I connected to the executing machine through the SSH service and collected the user flag. However, the major headache which was becoming apparent was to get the root access to read the root. txt file.

Following this, I would go through enumeration techniques on the found pathways such as; User’s home directory, running processes, ssh directory listing, bash history and crontab. The next step was to use “sudo -l” to list privileges of the user to the system, and I noted that the user nearly had root access to the /bin/tar command. Using the misconfiguration uncovered, I activated the command available on GTFOBins to gain the root access and complete the mission with the last flag.

#### Conclusion:

Trying to solve Bounty Hacker CTF was also a good practice which allowed to understand how enumeration works and how it is possible to approach privilege escalation in atypical manner. It further supported the notion of different attack scenarios and the essence of getting to know a system as much as possible in order to potential weaknesses.
This kind of walkthrough is to remind the reader that mastering cyber security is a life-long experience and each level of the challenge is a good opportunity to broaden your knowledge and enhance your skills. In this thread, I shall add my notes – ideas and observations, to the collective database, and hope that the information proved beneficial by some other person(s) who find themselves on the same learning curve as me – the exciting world of cyber security.