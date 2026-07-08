# Week 1

**Dates:** 06-16 to 06-25

## Goals
Task 1: Get Buckaroo set up and running on my computer
Task 2: Pick out some summary stats that may be helpful for the LLM to work with
Task 3: Familiarize myself with Buckaroo database by figuring out how to generate summary stats from the dataset and saving them off somewhere (like a json)
Task 4: Play around with Buckaroo app & read the paper to understand what it does & how it works

## Approach and Implementation

### Task 1:
The set-up required more time than I expected since the instructions in the README of the repo were a bit vague. (Only after did I realize that some branches had better instructions! Oops!) I needed to set-up PostgreSQL on my computer which was a pain as someone who doesn't know anything about SQL! Fortunately, with enough Googling and looking through the code base for what my PostgreSQL was supposed to be set up like and fixing a few path problems in the code, I figured it out and had Buckaroo running on my computer.

### Task 2: 
I did a bit of research on the "basic" summary stats that are most used / most useful. There are so many different kinds of summary stats and a lot of them do the same things, so it was difficult to choose between them. In the end, I just picked out the most common ones and my mentor and I agreed that we could add in the less common summary stats later and figure out which of them perform best (with the LLM) through trial and error.

### Task 3:
This task was quite difficult as a good amount of students & professors had already done a bunch of work on this codebase. The frontend is done in React while the backend was done with Flask, both of which I had never really worked with before. In addition, I had also never worked with SQL before, which was how the data set was being stored. 

Eventually, I somewhat got the hang of navigating the codebase and began to slowly make connections between the dozens of scripts. Though the goal was to put the generate summary stats and put them in a "Data Profile" table in the SQL database, since I was still getting used to SQL, my mentor just let me save it off to a json for the time being. That would be a task for next week.

### Task 4:

After reading the paper, I played around with the Buckaroo app for a little bit to get a better understanding of how it worked and exactly what it did. Being able to actually navigate through the app myself really helped to familiarize myself with the system.


## Results

By starting off with a small task given by my mentor, I was able to familiarize myself with the code base and the Buckaroo app without too much frustration and overwhelm! The set up process (specifically with the set-up of PostgreSQL) also provided me with valuable information that will definitely help me understand the various components of Buckaroo in the coming weeks.


## Notes
Met in person with mentor on 06/23/25 at the University of Utah. Established method of communication through Slack with mentor in case I have questions throughout the week.



