---
Title: Journal 9
categories: [SWS101, CTF Journal]
tags: [SWS101]
---

### Topic : Crack The Hash - TryHackMe Walkthrough 

#### Introduction:

I'll be sharing my experience and the actions I did to finish the TryHackMe "Crack The Hash" room in this journal post. Password cracking is a critical ability in penetration testing and security assessments, and it is the emphasis of this room. The area discusses several hashed password kinds and the methods for cracking them.

#### WalkThrough:

Task 1:

The first task involves cracking various hashes using different techniques and tools.

- Question 1:

Hash: 48bb6e862e54f2a795ffc4e541caed4d
I analyzed the hash format and determined that it could be either MD5 or MD4. To crack it, I used John the Ripper with the Rockyou.txt wordlist. John the Ripper requires three things: hash format, wordlist, and the hash itself.

- Question 2:

Hash: CBFDAC6008F9CAB4083784CBD1874F76618D2A97
The hash format analysis revealed that this hash could be SHA1. I used Hashcat to crack it. Hashcat requires two flags: -a for attack mode (default is 3 for brute force) and -m for hash type. The -m value for SHA1 is 100.

- Question 3: 

Hash: 1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032
The hash type is SHA2-256. For this one, I used an online tool called crackstation.net, which successfully cracked the hash.

- Question 4:

Hash: $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom
This hash is a bcrypt hash, which has a code of 3200 for Hashcat. Online tools might not always work for complex hashes, so I resorted to using Hashcat. To speed up the process, I filtered the Rockyou.txt wordlist to only include 4-character words, as hinted by the room.

- Question 5:

Hash: 279412f945939ba78ce0758d3fd83daa
I identified this hash as MD4 and tried cracking it with Hashcat using the code 900. However, Hashcat exhausted the wordlist without finding a match. In such cases, it's worth trying online tools like crackstation.net, which successfully cracked the hash.

Task 2:

The second task introduces the concept of salted hashes and requires cracking them using various techniques.

- Question 1:

Hash: F09EDCB1FCEFC6DFB23DC3505A882655FF77375ED8AA2D1C13F640FCCC2D0C85
I used crackstation.net to crack this hash quickly.

- Question 2:

Hash: 1DFECA0C002AE40B8619ECF94819CC1B
Similar to the previous question, I attempted to crack this hash on my own.

- Question 3:

Hash: $6$aReallyHardSalt$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02.
Salt: aReallyHardSalt
This hash starts with $6, which indicates that it could be a sha512crypt hash (code 1800 for Hashcat). Cracking this hash can take a significant amount of time, but the room provides the answer: waka99.

- Question 4:

Hash: e5d8870e5bdd26602cab8dbe07a942c8669e56d6
Salt: tryhackme
For this question, the salt is given but not added to the hash. I concatenated the hash and salt to form the final hash. Using the hash analyzer, I determined that it is a SHA1 hash. Hashcat has multiple SHA1 formats, and based on the hash format (password+salt), I tried the codes 110 and 160. Code 160 successfully cracked the hash.

#### Conclusion:

Practical expertise with a variety of hashing algorithms and password cracking approaches was offered in the "Crack The Hash" area. The main stages were determining the kind of hash, choosing the right tools (like Hashcat, John the Ripper, or internet tools like crackstation.net), and cracking the hashes using wordlists or brute-force assaults.

This room served as a reminder of the value of salting password security and the relevance of comprehending various hashing algorithms and their features. It also emphasized the necessity of strict password restrictions and the possible dangers of using weak or simple passwords.

With everything considered, finishing this room improved my understanding of and ability to crack passwords, which is an essential part of penetration testing and security evaluations. It underlined how crucial it is to keep abreast of the newest methods and instruments available for password security.
