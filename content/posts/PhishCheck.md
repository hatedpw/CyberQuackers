---
title: "A simple phish leads to a billion dollar company being breached"
date: 2022-10-07
draft: false
URL: "/posts/a-simple-phish-leads-to-a-billion-dollar-company-being-breached"
tags: ["CyberSecurity"]
---

When we think of a company getting breached generally, people think of some advanced attack that took months of planning and execution. But in reality, most breaches are caused by simple mistakes. So in this post, I will be going over a breach that could likely happen in the future and how it could have been prevented.

So let us start with the basics. What is a breach? A breach is when an adversary gains access to a system and steals data. This can be done in many ways, but the most common way is through phishing. Phishing is when a threat actor sends a fake email to a user and tricks them into clicking a link or opening an attachment. This is a widespread attack vector that many adversaries consistently use.

This story starts with a simple but effective phish.

![1](../Billionbreachimg/stage1.png)

You've opened up an email, and it's demanding that you sign these important documents that need to be reviewed, and you need to do it now. You click the link and are taken to a legitimate website; This is the official box domain, a trusted domain in which many users share documents all the time. So you let your guard down and read further. 

It says to click here to read the document. Oh, that's weird.. but is hosted on an official website, it must be fine. So you click the link and are taken to a page that looks like this.

![2](../Billionbreachimg/stage2.png)

This looks like 365 web view for word document editing, but the key difference is the URL. This is not the official portal.office.com URL. This is a URL that is hosted on a domain that Microsoft does not own. This is a phishing site. You are prompted with a login screen, and you enter your credentials. You click login, and nothing happens. It just says error wrong password or email, please try again. 

You repeat this process a few times, and you get frustrated. You think, "I know my password is correct, I just changed it yesterday, and I know my email is correct. I just sent an email to myself to check it. So why is it not working?" You then think, "Maybe I need to change my password again, maybe I forgot it." But each time you click login. The username and password were sent to the threat actor and saved into their database. 

The credentials have been stolen, and the threat actor can now login to your account and do whatever they want. So, for example, they can send emails to your contacts, delete your files, and even download them. You might think I am just a low-level person who cares if I get phished, right? Wrong, you have access to very sensitive data, and stealing a single account, even one that isn't important now, can lead to even more significant breaches later down the line through internal phishing attacks and lateral movement inside the network.

This is a very simple and straightforward attack used by thousands of adversaries daily. Why? Because it works. 

So how can we prevent this? 
1. ALWAYS check the URLs; if it doesn't look right, stop and alert your IT Team!
2. Think, should I be getting this email? Does it make any sense? Do I know this person?
3. Communicate with co-workers. Did they receive this to? Why would Jim, the intern get this invoice as well?
4. If you are unsure, don't click the link, don't open the attachment, dont enter your credentials. Report the email to your IT team. They will assist you as it has most likely been sent to everyone around you. 

The most crucial step is NEVER to feel scared to reach out to your IT team. Everyone, including security professionals, will fall for a phish at some point in their life. All it takes is that you aren't paying attention one time, and boom, you've just given up your password. Reporting these incidents allows IT staff to investigate and resolve the issue before it can cause damage to the company.

Understand that taking these steps will never fully guarantee your safety from phishing attacks but can help reduce your likelihood of getting phished. 

# Okay but what about the billion dollar breach? 
![3](../Billionbreachimg/stage3.jpg)

I was able to obtain access to the database where the passwords for this phish are stored, when I first looked at the list, it only had around 20 email/passwords stored, but only five hours later, it had over 260 stolen credentials. Many of these belonged to managers and staff from companies estimated to have over a billion net worth. 

Don't let this happen to you. Be vigilant and always be on the lookout for phishing emails.

Disclaimer: I have reported the location where the log files are being held, and until the website is taken down, I am monitoring the data being added to it and will then submit the information to https://haveibeenpwned.com/ to alert users of the breach.



Phish IOCS:

hXXps://hulking-citrine-krypton[.]glitch[.]me/flk[.]html
hXXps://ssvilvensstokes[.]app[.]box[.]com/notes/1033258185693?s=7b1zk6io9kmxqnau2agt3pr56e6czuwu