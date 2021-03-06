---
layout: post-no-feature
title: "A Front-end Journey of Accordium"
description: "Re-thinking on how Accordium front-end app should be."
category: articles
tags: [react, reactjs, best practice, corporate, guidelines]
---
[DRAFT]
I joined Accordium on mid of January 2018. It was Accordium's 10 months old running as a company. In my early days in Accordium, my development scope leant toward Backend development using Java, Kotlin, & Python. While April 2018 onwards, I code front-end more.

## Migration to React 16
As a disclaimer, my decisions on coding related, infrastructure, and development methodology are not because of a coolness of something. 

It was on April 2018, I realized that our front-end stack is too outdated to the point where it limit us to develop the system further. Not to mention how poorly the coding is done. No blaming here, as there were 2 reasons for it:
1. As a startup, we have very little time to develop the apps but we have to ship. There was not much reference on what should Accordium build that time.
2. Prior to React 16 version: I, personally, don't like React Framework before React 16. React is 'sold' as unopinionated JS framework and this is the part I don't like for a JS framework. JS itself is not a powerful language, it allows many things that other languages won't allow. by having too much freedom on doing things, the goal of react being a 'virtual dom' framework will be hardly fulfilled by those React developer new comers. 

It was happened in Accordium, after checking the code one by one, the usage of DOM element queries are beyond my expectation. React was used only as UI templating, as if it was chosen because it is cool. This is the very problem when I did migration to React 16. React becomes more strict, things that are unpredictable simply doesn't work (or sometimes it works sometimes it does not). For an instance, document.getElementById will not return any dom element as it does not actually know when the DOM is exist in the document (even you put it in componentDidMount 😀). As the quick patch, I convert all the direct document queries by using React refs. The question will raise, "Refs is not 'correct' either, why don't you write a proper code for handling that". The answer is business and resources. 

1. Business: We can't have a long service disruption because it will affect our customers trust while we are still trying to gain their trust. To be frank, on that time, our customer impression of our system is cool UI but buggy.
2. Resources: In my previous company, I was a team lead of front-end team and one major thing I learn is not every developer is immediately willing to follow standard and guideline define by others. So having the resources ready for the change needs time.

By the reasons above, I migrate the apps in a very minimal changes as I can because the most important thing of changes is **to start**.

## Rewrite Accordium Apps & Coding Guidelines
Since then I wrote a coding guideline and standard as my defense in convincing the team that we need to "redo" this app at least 70%. Why not 100%, same reason as before; business and resources. It reminds me of writing a WCAG 2.0 Level AA guideline for my first company I work to. One thing that should be noted of writing this kind of document is probably on 20% of your team really care to read it. Why it is still a good thing then? it shapes your habit of coding, a good one when you read, think, then write.
 On June's company meeting, it was decided that we will use business' summer break to rewrite the apps. 
 
 It was worth it, We have much lesser evening/midnight support as our apps is now considerably stable.

## Compromising, Team Work

## Major Upgrade, Timing

## What's Next
### Accessibility
### Accordium UI Component Toolkit
