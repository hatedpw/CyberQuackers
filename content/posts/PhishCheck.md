---
title: "A simple phish leads to a billion dollar company being breached"
date: 2022-10-07
draft: false
URL: "/posts/a-simple-phish-leads-to-a-billion-dollar-company-being-breached"
tags: ["CyberSecurity"]
---

When we think of a company getting breached, gerenerally people think of some advanced attack that took months of planning and execution. But in reality, most breaches are caused by simple mistakes. In this post I will be going over a breach that could likely happen in future and how it could have been prevented.

So lets start with the basics. What is a breach? A breach is when a adversary gains access to a system and steals data. This can be done in many ways, but the most common way is through phishing. Phishing is when a threat actor sends a fake email to a user and tricks them into clicking a link or opening an attachment. This is a very common attack vector and is used by many adversaries.

This story starts with a simple but effective phish. 

![1](../Billionbreachimg/stage1.png)

You've opened up an email and its demanding that you sign these important documents that need to be reviewed, and you need to do it now. You click the link and are taken to a website that is all legitmate, This is the offical box domain, a trusted domain which many users share documents all the time. So you let your guard down and read further. 

It says to click here to read the document, oh thats weird.. but oh well its coming from the offical domain so it must be fine. You click the link and are taken to a page that looks like this.

![2](../Billionbreachimg/stage2.png)

Visually this looks exactly like 365 web view for word document editing, but the key difference is the URL. This is not the offical portal.office.com URL. This is a URL that is hosted on a domain that is not owned by Microsoft. This is a phishing site. You are prompted with a login screen, and you enter your credentials. You click login and nothing happens, it just says error wrong password or email please try again. 

You repeat this process a few times, and you get frustrated. You think to yourself, "I know my password is correct, I just changed it yesterday, and I know my email is correct, I just sent an email to myself to check it. So why is it not working?" You then think to yourself, "Maybe I need to change my password again, maybe I forgot it." But each time you clicked login. The username and password was being sent to the threat actor and saved into their database. 

The credentials have been stolen, the threat actor can now login to your account and do whatever they want. They can send emails to your contacts, they can delete your files, they can even download your files and send them to their own email. You might think oh, I am just a low level person who cares if i get phished right? Wrong, you have access to very sensitive data, and stealing a single account, even one that isn't important now can lead to even bigger breaches later down the line through internal phishing attcks and lateral movement inside of the network.

This is a very simple attack and is used by thousands of adversaries every day. Why? Because it works. 

So how can we prevent this? 
1. ALWAYS check the URLs and if it doesnt look right, stop and alert your IT Team!
2. Think, should i be getting this email? Does it make any sense? Do i know this person?
3. Communicate with co-workers, did they recieve this to? Why would Jim the intern get this invoice?
4. If you are unsure, dont click the link, dont open the attachment, dont enter your credentials. Report the email to your IT team. They will assist you as it has most likely been sent to everyone around you. 

The most important step is NEVER feel scared to reach out to your IT team. Everyone will fall for a phish at some point in their life, security professionals, literally everyone. All it takes is that one time you aren't paying attention and boom, youve just given up your password. Reporting these incidents allows for IT staff to investigate and resolve the issue before it can cause damage to the company.

Understand taking these steps will never fully guarentee you safety from phishing attacks but can help reduce your likelihood of getting phished. 

# Okay but what about the billion dollar breach? 
![3](../Billionbreachimg/stage3.jpg)

I was able to get access to the database where the passwords for this phish are being stored, when i first looked at the list it only had around 20 email/passwords stored, but only five hours later it had over 260 stolen credentials. Many of these belonged to managers and staff from companies that were estimated a net worth over a billion dollars. 

Don't let this happen to you. Be vigilant and always be on the lookout for phishing emails.

Disclaimer: I have reported the location the log files are being held and until the website is taken down am monitoring the data being added to it and will then submit the information to https://haveibeenpwned.com/ to alert users of the breach.



Phish IOCS:

hXXps://hulking-citrine-krypton[.]glitch[.]me/flk[.]html
hXXps://ssvilvensstokes[.]app[.]box[.]com/notes/1033258185693?s=7b1zk6io9kmxqnau2agt3pr56e6czuwu