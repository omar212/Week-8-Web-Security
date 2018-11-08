# Week-8-Web-Security

# Project 8 - Pentesting Live Targets

Time spent: **7** hours spent in total

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

Vulnerability #1:  Session Hijacking/Fixation
Description: Fisrt login to the blue section, change it the url to public/hacktools/change_session_id.php to get the session ID. Then i opened safari doing the same process and copy and paste the session id from the last browser change the session ID. In result you will automatically be logged in.
- [x] GIF Walkthrough: 
     - <img src='BlueSessionHijackingFixation.gif' title='XSS' width='' alt='' />




Vulnerability #2: SQL injection
- Description: I tested the blue section and it result shows that the "Database query failded", and others can redirect the page.  I used the SQLI " '?id=' OR 1=1'--' " to achieve this
- [x] GIF Walkthrough: 
     - <img src='Blue SQL Injection.gif' title='XSS' width='' alt='' />


## Green

Vulnerability #1: Cross-Site Scripting
-Description: Going into the contact page, enter your name,email, and feedback. For example " '<script>alert('Omar found the XSS!')</script>'" then go to the feedback by logging in. The alert should pop up.
- [x] GIF Walkthrough: 
     - <img src='Green Cross Site Scriptiting.gif' title='XSS' width='' alt='' />


Vulnerability #2: Username Enumeration
-Description: Similar to last week, when you test the correct username, the inspect page will show "failture". when you test the wrong username, it will show "failed".
- [x] GIF Walkthrough: 
     - <img src='Green User Enumeration.gif' title='XSS' width='' alt='' />


## Red

Vulnerability #1: Cross-Site Request Forgery (CSRF)
-Description: First Login and go into the Users page for each blue,green, and red. Enter the edit page and change the value of csrd_token the name gets changed. However that only works for the red section works and the blue and green page gives you a Error: invalid request
- [x] GIF Walkthrough: 
     - <img src='Red CSRSF.gif' title='XSS' width='' alt='' />


Vulnerability #2: Insecure Direct Object Reference (IDOR)
-Description: Went to each blue, green, and red page and under Find Sales Person, click any user and change the id on the url with numbers 8-12 till I found the salepersons who are not in the list in the red page.
- [x] GIF Walkthrough: 
     - <img src='Red IDOR.gif' title='XSS' width='' alt='' />


## Bonus Objective 2: Build on Objective #4 (Cross-Site Scripting)
-Description:Entering the green feedback section, You can enter a <script>document.location="https://www.facebook.com"</script> and when you go back to the feedback page, it will should direct you to facebook page.
- [x] GIF Walkthrough: 
     - <img src='Bonus Objective 2.gif' title='XSS' width='' alt='' />


## Notes

Describe any challenges encountered while doing the work
