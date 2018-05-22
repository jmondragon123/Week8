# Project 8 - Pentesting Live Targets

Time spent: **12** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1:Session Hijacking

Vulnerability #2:SQL Injection



## Green

Vulnerability #1: User Enumeration
	When an existing user enters the wrong password the error message is returned bold. When a non existing user enters a 
	password the error message is returned not bold.

Vulnerability #2: Cross-Site Scripting
```
Look</td><IFRAME SRC=“javascript:alert(‘Jorge Mondragon’);”></IFRAME><td>HI
```
```
Look</td><IMG SRC="#" ONERROR="alert('JorgeMondragon')"/><td>HI
```
## Red
Vulnerability #1: Insecure Direct Object Reference
```
	https://35.193.161.23/red/public/salesperson.php?id=10
```
```
https://35.193.161.23/red/public/salesperson.php?id=11
```

On the Green and Blue website, whenever an id value over 9 is inserted the website redirects the user to the 
salesperson landing page.

Vulnerability #2: Cross-Site Request Forgery



## Notes
It was hard figuring out how to create a form to do Cross-Site Request Forgery until I looked back at notes. SQL Injection was the hardest since it is where I have the least knowledge on. Overall this assignment was extremely fun.


## Concept Review
1. The easiest attacks were Username Enumeration and Insecure Direct Object Reference. The harder attacks were SQL Injection and Cross-Site Scripting.

2. The easiest way to prevent username enumeration is to have a consistent message for valid and invalid inputs.

3. Another place that could be vulnerable would be when accessing the territories. I would remove showing the id in the URL to try to prevent IDOR.

4. If you use an AND statement instead of an OR statement when doing SQLI the machine will try to check if both statements are TRUE instead of checking if one statement is TRUE. The AND statement only will work if the submitted field and the code are correct.
5. A method to get a response to a website that the attacker is hosting. For example a javascript file with malicious code on a website being hosted by the attacker.

6. I would send them an email with the page saying that if they click the button they can win a prize.

7. I believe that the easier attack to execute would have to be session highjacking because if you are able to sniff the wifi and find their session then the attacker can change their session to match the victims. Session Hijacking is easier to defend against because the developer can have the session token change.

## GIF's


1. Session Hijacking:
![](https://github.com/jmondragon123/Week8/blob/master/SH.gif)
2. SQLI:
 
3. User Enumeration:
![](https://github.com/jmondragon123/Week8/blob/master/UE.gif)
4. Cross Site Scripting:
![](https://github.com/jmondragon123/Week8/blob/master/XSS.gif)_
5. IDOR:
![](https://github.com/jmondragon123/Week8/blob/master/IDOR.gif)
6. CSRF:
![](https://github.com/jmondragon123/Week8/blob/master/CSRF.gif)
