---
layout: default
---

# Week 03

[← Back to Home](../index.md)

## Documentation 

For this week, we start off with sharing with our peers what we did for our interactive data portrait. I did talk about wanting something stars related in week 1- once I have processed all of my data. I knew I wanted the stars to be interactive, or at least have different shapes to distinguish what data its expressing. Using colors, sizes, etc. 

I haven't started yet during this time. But I looked at my peer's work which gave me more inspiration on what to do. Another example I looked at was the "data structure garden" on p5.js website. I really liked how the flowers "bloomed" and when you go to click on the canvas it would generate new ones. I also understand that the data portrait should be more interaction based, and also that it shouldn't include text and have a more abstract apporach to expressing. 

# In class activities

Through digital and analogue approaches, explore how to access, filter, and translate live data into visual and material forms. These activities build on the coding fundamentals from Experiment 2, while also introducing analogue practices rooted in rule-based and generative design.

We explored with curl, which is a free and open-source command line tool for transferring data over the Internet. Allowing user to send a request to a web address and shows what comes back. We worked with live data, an example being looking at the weather here in auckland. 

![Alt text](../assets/week-03/akl.png)

Also places like Tokyo and Shanghai, I have also managed to explore and change the languege of which the data pops out on. 

![Alt text](../assets/week-03/tk.png)
Tokyo weather 
![Alt text](../assets/week-03/SH.png)
Shanghai weather

I found this very interesting since its all worked in the windows terminal. I did however struggle with finding the moon phases and synonym. 

I also looked at how to draw with the weather, using a specific code I could see how the drawing change. 

![Alt text](../assets/week-03/蓝圈.png)
This is what the original code looks like, 

![Alt text](../assets/week-03/天蓝.png)
And this is after I changed some numbers, which makes the color lighter. I also tried putting through my own codes. which didn't work as a function and I couldn't figure out why. It irratated me alot. 

**UPDATE**

I actually did figure it out. I may be slow. 

I noticed that it wasn't about the numbers but to reset the the latitude and longitude in the weather forecast API, and reselected the current temp, current humidity and current wind. 

![Alt text](../assets/week-03/silver.png)

The area set to Silverdale, in auckland 

I couldn't figure out how to add ranom() and noise() function to the code. So I did vibe coding, and this is what I got:

![Alt text](../assets/week-02/hi.gif)

which made it look really funky while it moved. I could also change the timeoffset to make it faster.

Besides this, I looked at ISS Tracker, this sketch calls the API every 5 seconds and updates a dot and text on the canvas.
![Alt text](../assets/week-03/dot.png)

## Indenpendent study

For my indenpendent study, I wanted to see what the weather is like in Shanghai, so I started looking in open meteo. I changed the latitude and longitude to Shanghai, China and reset the timezone to auto detect. Then I picked out the variables, being current temp, relative humidity, wind speed, and sea level pressure. 
