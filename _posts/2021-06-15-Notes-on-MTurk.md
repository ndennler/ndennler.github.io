---
layout: post
title:  "Notes on Conducting MTurk Studies"
date:   2021-06-15 08:00:00
blurb: "My experience running online studies."
og_image: /assets/img/content/post-example/Banner.jpg
---

Nathan’s Notes on Mechanical Turk:
(HIT = Human Intelligence Task, which is the thing that a worker signs up for when you put a study on MTurk)

1. Pay workers!

    More of an ethical thing, but some people doing mechanical turk need this to live. Definitely make pilot studies and time them to see how long it would take for a person who is moving at a reasonable pace to complete the study, and base the payment on that. Also, a lot of turkers have additional tools that help them find high-paying HITs, so paying them helps you too :3.

2. Mechanical Turkers will not read the consent form (put payment info in the task description)
    In the study I did, the turkers were paid by the number of robots that they rated, following Maja’s above statement. This was very clear (bold, highlighted in red) in the consent form  but many workers complained about the study being too long for what they were paid, because the listing was for 1 robot. This potentially caused some of the turkers to feel mislead and complain about the payment (which was set to $15/hour based on pilot study times with friends). 

3. Mechanical Turkers have several websites where they communicate with other turkers about how good different tasks are, which can help or hinder the recruitment process.

    In my experience, the two that I found were: 
    “https://turkopticon.ucsd.edu/” and “https://turkerview.com/” 
    These websites rely on users to write reviews, so you may or may not be listed on the website. They also rate by the requester, so if there is a lab account that does poorly paid studies, this can negatively impact other studies done by the lab.

4. Most workers are bots. Use restrictive criteria.

    The two main methods of restricting who can take the HIT is “# of HITs completed” and “% of HITs accepted”. The optimal parameters I found for a study conducted in the summer of 2020 was 1000+ completed HITs and >99% acceptance rate. This is far more restrictive than many studies I have seen, and yet ~10% of the responses were basically walls of copy-pasted text. An example when asked to describe a robot pictured on their screen (verbatim, from several different participants): 
    “Boston Dynamic’s dog-like SpotMini robot is to go on sale in 2019. This cute and uncannily realistic canine-bot is just one of many robots that are inspired by the natural world. Human engineers increasingly look to living systems for clues to a good design, whether it be emulating an insect brain’s ability to navigate or building robots with bacterial stomachs that produce electricity.”  - Countless Participants

5. Have some method in place to identify negligent users or bots.

    I think one good way to do this is to ask qualitative questions about what phenomenon you are measuring. For me, I used open-ended questions on every survey as one method. This can give really interesting information anyway, and it also helps identify users that do not answer the question (It is hard to use this as criteria for exclusion other than the copy-pasted answers, but it can give you a good idea). Sometimes people type in all caps too and it sometimes doesn’t make sense, but the jury is out on whether or not those people are robots or perhaps just older participants or participants where English is not their first language (who absolutely should still be included in analysis). The other option is to use validated scales. This helps identify people who are answering randomly, as their personal intrarater reliability will be quite low for the same construct. If you use a validated scale, there is a precedent to exclude participants who have 95% CIs for cronbach’s alpha that do not contain the validated scales reported cronbach’s alpha. A third thing you can do is include positively and negatively phrased questions, especially if they are already on the same scale to identify when someone might not be paying attention, by seeing that there should be generally opposing sentiments for the two questions for the same stimulus. You can also check if people are only answering undecided for everything. Whatever you do, it is important to write about what you did and why when conducting the study and excluding participants.

6. I strongly recommend using the python interface to handle payment of HITs (make sure you know the workers’ MTurk ID through your survey, so you can inspect their answers)

    This basically gives you a json of who completed the HIT, and there are API calls you can make to send money from your account to the worker as well as post the HIT. This makes it a lot easier to post HITs.  It is actually documented pretty well: https://docs.aws.amazon.com/AWSMechTurk/latest/AWSMturkAPI/Welcome.html 
    Another note is that if you post more than 10 HITs at a time, you incur an additional cost, so one way to cut some costs that would otherwise go to amazon is to only post HITs that are limited to 10 respondents and then review them and repost them. I also think this is good in general for iterative evaluation of how the study is going.

“Fun” Gotchas:
- Approval rating is stored as an int, so if you say >99% approval rating, you will only be able to get turkers with a 100% approval rating. Use >=99% instead.
- Time kind of matters too! Most of the time doing a tuesday deployment at 10AM PST will give you good results.
