---
layout: default
---

# Week 10

[← Back to Home](../index.md)

## Documentation 
1. Progress Reports

Share your progress report slideshow with a small group of peers. Before presenting, make sure your feedback questions are clearly communicated so the group can respond to them directly.

Each person has 5 minutes to present, followed by group discussion and feedback. Assign the roles of Chair, Technical Commenter, and Conceptual Commenter for each presentation, rotating roles after each presenter. Post comments to the presenter's card on your group's Padlet boardLinks to an external site. across the four feedback columns. Record the feedback you receive for your journal entry.

Review the cards on your group's board and add any further comments or suggestions not raised during the live critique.

In class, We had another progress check with our peers and had written reviews on Padlet. 

![alt text](../assets/week-10/Screenshot%202026-05-29%20115003.png)

Here is the feedback I have received. 

2. Gallery Walk

Visit the other groups' Padlet boards (you can access these via the main class Padlet boardLinks to an external site.). Browse their Technical and Conceptual feedback cards, and add a comment or suggestion of your own via "+ Add comment" or "+ Post". Use the heart (like) button to upvote the most helpful advice.

3. Action Plan

Drawing on the feedback from the critique session, write a short reflective summary for your journal (around 250 words). Identify the most significant feedback and ideas you encountered, and establish clear, concrete action points to develop your project.

There hasn't been a major pivot in my project direction, rather, I've focused on clarifying how I will technically achieve the final outcome. Feedback was minimal, but one critical question emerged. Do you have a backup plan if the original technical approach fails?

My original plan establishes a three-part data pipeline: Figma serves as the interface where participants select a colour and enter a few words to express their feeling. That input connects to a Google Sheet, which acts as the live database. From there, a p5. js script reads the sheet and generates the real-time visualisation. A large-scale projection of overlapping, glowing forms that collectively maps our community's emotional "chromatics"

However, I recognise that Figma's native capabilities for writing to external databases are limited. API latency or authentication hurdles could break the chain. Therefore, my backup plan, shaped by peer feedback, replaces Figma with a Google Form. Participants would still choose a colour and describe their state, but the submission would flow directly into the same Google Sheet without requiring Figma. The p5.js script would then read from the sheet identically, preserving the installation's core experience.
This backup maintains the low-friction, anonymised, voluntary data model while reducing technical risk. It sacrifices some interface customisation for reliability, ensuring the collective emotional portrait remains the priority, not the fragility of the toolchain.

## **Independent Study** 

Project development is the sole focus of this week's independent study. Make use of the critique session and the action plan developed from class to guide your work.

Document your progress, including both textual and visual evidence. Reflect on what you tried, what you learnt, and how this has moved your project forward. Keep in mind that you have two weeks to complete the project for the showcase in week 12.

From this, I focused on looking into possible ways to plug in figma and connect it to google sheets. From my research I found that It is possible with a plug in.

![alt text](../assets/week-09/plug.png)

However, the more I tested the more I realized this isn't what I wanted. The plugin allowed me to sync the data from the sheets to figma and not the other way around. I have yet to find a possible solution to this issue. Every research I have done is around the same results. 

I started looking for more solutions to this issue. I'm sure there are better solutions that would allow figma to do this (or even use a different interface) but this But with time running out, I figured I would just use the backup plan and change from figma to google forms. 

So I chose to pivot.

Giving up figma, I looked into using google forms. So its simply a QR code link to a google form, then linked to google sheet, which is then connected to the p5.js sketch. 

Since I want my form to have the option of choosing and customizing the colours, I realized that it's not possible to have that in google forms. So I started looking at other form applications that allowed me to have that option. 

I landed on "jotform." Which is a platform specifically made for forms and they have a widget option. 

![alt text](../assets/week-10/jot.png)

They also have the option to connect and link to a google sheet, which is wonderful :0 

That didn't take long to set up, I chose to use personal account to set the sheet just because the uni email seems to be blocking it. 

![alt text](../assets/week-10/feel.png)
(it wasn't working for a bit so I let my anger out...I also asked my friends to test too...figured this is a pretty solid data)

Now the hard part is getting this to connect to the p5.js sketch. With the rapid prototype I have done before, I really liked how the coloured blobs looked. I figured to just use that as base, and look up videos on how to link it to sheets. 

I found a youtube video from David Bouchard (David Bouchard, 2021), and learnt how to publish my data set into something public and copying the link into a CSV link. 

I also learnt a new function, called preload on p5.js. Which is A function that's called once to load assets before the sketch runs.(Preload, 2024) Along with loadTable function, which reads the contents of a file or URL and creates a p5.Table object with its values. If a file is specified, it must be located in the sketch's "data" folder. The filename parameter can also be a URL to a file found online. By default, the file is assumed to be comma-separated (in CSV format). Table only looks for a header row if the 'header' option is included. (LoadTable, 2025)

I bumped into some issues though however, In the video he used the consol to make his form on the scripting tool he's using. I soon realized I don't have that so looked for other options. 

I looked into more research, so in order to pull data from Google Sheets into p5.js without a console, publish your sheet as a CSV and use p5's loadTable() function inside preload(). This allows me to store sheet data directly in variables and display it on your canvas. (David Bouchard, 2021) 

![alt text](../assets/week-10/66.png)

I added this to my previous sprint (the coloured blob) 

Obviously this didn't do anything because I didn't set up the other functions. So I had to google some more 

![alt text](../assets/week-10/set.png)

There is something called setInterval() function which allows me to grab new data everytime the source is refreshed. (at least thats how I understand this) I looked at the over view that is provided, and also looked into other examples that are online. 

<iframe src="https://editor.p5js.org/re7l/full/zt2ZJrpgo" height= "400" width="400"></iframe>

Using this one for example by re71 on p5.js, This function cycles through an array of words every second by incrementing the index each time changeWord() is called (by setInterval), and when the index reaches the end of the array it resets to 0, creating a looping word display at the center of the canvas.

![alt text](../assets/week-10/eq.png)

**So could I apply the same logic with my data sheet?**

## **Reference**
David Bouchard. (2021, September 21). RTA842 - 3.1 - Working with spreadsheets in p5.js. YouTube. https://www.youtube.com/watch?v=EU7SvAyybOE

loadTable. (2025). P5js.org. https://p5js.org/reference/p5/loadTable/

‌
preload. (2024). P5js.org. https://p5js.org/reference/p5/preload/

‌
‌