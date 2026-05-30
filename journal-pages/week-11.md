---
layout: default
---

# Week 11

[← Back to Home](../index.md)

## Documentation 
1. Journal Review

Work in pairs. Using the Journal Checklist Download Journal Checklist, review your partner's journal entries for weeks 6–10, checking for clarity and completeness, an effective balance of visuals and text, and correct technical implementation. Share your observations with your partner.

Then re-read your own journal entries in preparation for the Studio Consultation. Identify three key moments (e.g. discoveries, challenges, decisions, feedback) that shaped your project direction. Write 1–2 sentences about each of these.

I have completed most of the blog entries at this point, but there are few things that I am lacking, I did went back in and refill them 


2. Practice Consultations

Work in pairs. Take turns interviewing each other using the question prompts on the class slides, following the same format as the Studio Consultation (10 minutes each). The interviewer should use the prompts as a guide rather than a script, ask follow-up questions, and let the conversation move between topics naturally.

Reflect on how you responded to the questions. Consider whether your answers were focused and coherent, and whether you were able to articulate how your work positions itself within broader ideas about data. Write 2–3 sentences about what you want to improve on, and keep these notes for your journal. Then find a new partner and repeat.

The feedback I have was helpful, I noticed I had the potential to go more into depth with the fourth question- How does your work challenge conventional ideas?- I could mention more of the social issues and how the future would look, why did I choose to do this? focus on that specific future? 

I certainly need more research, and rewrote my future scnario down to keep as a reminder. 

**"A city where public areas serve as emotional mirrors, enabling strangers to use touch-driven digital interfaces to silently perceive, acknowledge, and gently influence each other's inner states, turning anonymous crowds into welcoming, sympathetic micro-communities without the need for verbal communication or the loss of personal privacy."**

3. Showcase Planning

Add yourself to the showcase Miro boardLinks to an external site. and mark your preferred location to install your work. Coordinate with the class to agree on a plan. Use the board, along with Canvas/Discord/etc. Be ready to install your work at 2 pm on Friday 05 June.


## **Independent Study** 

I kept working on my project, at this stage I needed to test out the setInterval and loadTable function, 

The code connects to the google sheet by using loadTable function to fetch the sheet data as a CSV file every second (by setInterval), then it converts each row of the spreadsheet into a moving blob on the canvas. The loadTable function takes four parameters. the published google sheets URL, When the data successfully loads, it's stored in the table variable, and then updateBlobs is called, which loops through every row using table.getRowCount function and table.getRow(i), extracts the "color" and "text" values from each row using row.get("column name"), and creates a new blob object with random position, size, and movement speed. 

However. Something went wrong and my sketch has no coloured circles but full plain ones... 

Here's a gif for better reference, (I tried to plug in iframe but it just looked blank)

![alt text](../assets/week-11/white.gif)

I don't know what went wrong. I have also double checked and fixed my google sheets when new answers/ inputs are put in, I realized that sometimes the collums would move and the hex strings would be shifted into the wrong place. This was an easy fix, but once refreshed, restarted the sketch didn't change and I couldn't figure out why. 

I was wasting away time at this point, I wanted to get this done as soon as possible. I went ahead and put it through AI to see what I did wrong. 

I prompt, "How could I make it so the blobs changes colours based on the hex string provided by the sheet source?" 

![alt text](../assets/week-11/c.png)

I knew that the url couldn't be the problem because I have seen it work. But it did mention that it's loading HTML instead of actual sheet data. So the color values was never proper hex strings. 

I tried the code that was given to me by Chatgpt for the blob updates. (trying something is better than nothing) But it didn't change much other than making the blobs more far apart and after a minute it would just disappear. 

I also wonder if it's because I didn't rename the row headers that why it wasn't picking up. 

...

WELL it's not. Because I changed that and nothing worked. I would need to go back to doing more research. 


## **Reference**

loadTable. (2025). P5js.org. https://p5js.org/reference/p5/loadTable/
