# DESCRIPTION
- 6/9/24: My first attempt at doing a TryHackMe challenge. 
- The basic idea of this challenge is to hack into (finding hidden directories and pages containing valuable info) of a fake bank website. 


# PART 1: Getting Started, and running GoBuster on HTTP site
![image](https://github.com/benjikenji/Project-2-TryHackMe-1/assets/115884414/83101a94-47fc-4f8b-83f6-37fb80f26aa9)

- After logging in to TryHackMe, we start up the first challenge, "Intro to Offensive Security". We then boot up the Virtual Machine that is provided by TryHackMe.
- I am first tasked to go to the Terminal and run "GoBuster", which is a command-line tool used to find hidden pages in HTTP and HTTPS websites.
- I do both of these things in the image above using the command ```gobuster -u www.fakebank.com -w wordlist dir``` . "-u" is supposed to denote the URL of the website to scan, and "-w" is supposed to denote the name of the wordlist file being used. The words in the wordlist are the keywords that GoBuster looks for when scanning a website for hidden pages.




![image](https://github.com/benjikenji/Project-2-TryHackMe-1/assets/115884414/b0d831a3-2141-460d-8d1d-1f538019853f)
- As seen in the Terminal above, GoBuster reports that there are two hidden directories for fakebank.com: ```/images``` and ```/bank-transfer```.
- ```/bank-transfer``` sounds interesting to me, so in the next step, I take a look by navigating to it in the Virtual Machines' web browser.


# PART 2: Navigation
![image](https://github.com/benjikenji/Project-2-TryHackMe-1/assets/115884414/eef64527-5797-4910-8356-4793a7cd4fa2)
- Upon entering in ```fakebank.com/bank-transfer``` into the URL search bar, I am greeted with a webpage that apparently allows me to transfer money to and from any account associated with the bank.

![image](https://github.com/benjikenji/Project-2-TryHackMe-1/assets/115884414/284a5e73-93ab-4d78-9393-ef2cc30ab63e)
- Like any malicious hacker would, I then decide to transfer $2000 from bank account #2276 (presumably some random person's bank account) to bank account #8881 (my account in this scenario).

![image](https://github.com/benjikenji/Project-2-TryHackMe-1/assets/115884414/3eb86014-bfa7-435a-973f-908ec81cec41)
- When clicking on "Return to Account", I see the key to the challenge from a pop-up notification. 

