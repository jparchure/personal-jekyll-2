---
layout: post
section-type: post
title: Dipping Toes
author: Jay
---

A fairly persistent question that bugs the minds of data science novices is- "Where do I start?"
For computer scientists, there is awlays Project Euler, LeetCode and HackerRank. The data science equivalent to it is Kaggle. <br>
So, the natural answer for the question is- "Go to Kaggle". But this answer does little to provide clarity. <br>
Or atleast it did not for me. <br><br>
A little bit of a background first. I am a professional data analyst who is used to working on industry projects that have well(ish)-defined requirements, end goals and a supporting team to move things along.<br>
In the wild wild west of Open data, it is very hard to find a structure that takes you beyond your standard Tutorial/MOOC material.<br><br>
I was in a similar predicament for the past few months. I often took a dataset, poked into it with Excel/R/d3/Tableau and after a while I got confused as to what was I looking for.
This exercise, though very beneficial did not lend me the satisfaction of solving a problem. After all, what did I achieve?<br>
So, this morning I was going through the same ritual, but on Kaggle.
I explored the dataset containing <a href="https://www.kaggle.com/kaggle/hillary-clinton-emails"> Hillary Clinton's emails </a>.
This time, instead of downloading the dataset I decided to look at what others had done.
However, I found a few highly rated scripts which addressed the foreign policy aspect in those emails. One of them, did a frequency analysis for all the countries in the world against those emails. The author mapped their results.
The second one did a sentiment analysis of those countries and created a bar graph. <br><br>
As I went through, forked and **rewrote** those scripts, I began to get an understanding of their code.
I made fairly minor and insignificant, mostly syntactical changes to the first script based on my programming style.
In the second one, it was clear to me that the visualization could be much more effective if it was a color coded map instead of a bar chart. So, inspired by the first script, I simply reworked the sentiment expressed about countries to a map and recolored to a diverging red-blue scheme.
The output was visually pleasing and IMHO was a better representation of a geographical data than a bar chart.<br><br>
But that I was able to read, understand and extend an existing piece of code was the most valuable outcome from this exercise for me. <br>
As a Kaggle lurker for about an year or so, writing my first snippet that extended an existing functionality was very encouraging.<br><br>
So my advice, if you feel unsure about a new dataset, simply take a look at what people have already done with it. **Rewrite** the code(this is important, **rewrite** instead of copy paste and if possible, make syntactical changes based on your programming style) and then see if there is someway you can make some addition to it.<br><br>
Sometimes, the changes might be as simple as modularizing the code, or like in my case, creating a new visualization, but this will get your creative juices flowing while giving you a better understanding of what is going on.
You can find my script <a href="https://www.kaggle.com/jparchure/d/kaggle/hillary-clinton-emails/map-of-country-sentiments">here</a>.
