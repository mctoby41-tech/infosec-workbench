# TryHackMe — Offensive Security Intro (Learning Log)

## Overview
A foundational lab introducing offensive security concepts, tools, and methodologies. Logged as part of my cybersecurity learning progression.

## Objectives
- Task #1 Think like a hacker
- Task #2 Starting the lab
- Task #3 Find Hidden Pages 
- Task #4 Attack the admin page 

## Concepts Covered

- ## 1 Offensive Security is about thinking like an attacker to find weaknesses before real hackers do.

~ In this room, you'll hack your first website in a safe and legal environment to see how ethical hackers operate.
Answer the questions below

~ Which term describes simulating a hacker's actions to find weaknesses?
~ Answer:  Offensive Security 
  
- ## 2 This room uses a virtual desktop to simulate a real system. A browser will automatically open, displaying FakeBank, a fake banking application. This is what you will be targeting.

~ 2 View Site
~ Answer the questions below
~ What is the bank account number in the FakeBank application?
~ 8881

- ## 3 Goal Find a weakness in the FakeBank application. One common mistake is leaving hidden pages accessible.

~ View Site
~ Open the Terminal
~ Open the terminal on the machine. You will be using this to run your first hacking tool, dirbuster. The terminal icon looks like this:
~ Finding Hidden Pages
~ To find hidden pages using Dirbuster, we will use dirb and the URL that we wish to search:
~ dirb http://fakebank.thm
~ Any lines from the output that start with + are pages that have been found. Dirb will find two URLs.

~ Answer the questions below
Dirb found one URL, http://fakebank.thm/images.
What is the other hidden URL?
http://fakebank.thm/bank-transfer

- ## 4 You should now have found a hidden admin panel that lets you add money to your account.

~ View Site
~ To open this URL in the browser of the simulated desktop:
  Add the following: 
  /bank-transfer
  to the URL in the browser.

~ Use your account number 8881 and deposit $2000 (or more). After depositing, return to your account page and confirm the balance is now positive.
Answer the questions below

~ When your balance turns positive, a pop-up with green text appears.

~ Enter the green words as the answer (ALL CAPS)
  BANK-HACKED 


## Tools Practiced
- Virtual desktop 
- Basic Linux commands
- Simple enumeration scripts
- TryHackMe in-browser attack environment

## What I Learned
- How to think like an attacker to find vulnerabilities before to find weaknesses before real hackers do.
- How hackers find a weakness in an application & exploit it.
- Find hidden pages using a tool (Dirbuster) & the URL to search for hidden pages.
- How hackers exploit hidden pages to add $$$ to their own accounts & than confirm the amount being transfered.  

## Defensive Takeaways
- Understanding attacker workflow helps build better detections

## Next Steps
- Complete additional THM offensive modules
- Document each lab with defensive takeaways
- Apply offensive knowledge to blue-team detection projects
