# Week 7

**Dates:** 07-30 to 08-06

## Goals

- Task 1: Get communication with LLM working
- Task 2: Get ablation study to a working state
- Task 3: Start cleaning up code, add documentation

## Approach and Implementation

### Task 1: 

This task was pretty tricky, mostly because although right now none of this ablation study code is currently touching the front end, I have to implement it in a way that would make it easy to implement in the front end in the future. So, I had to figure out a system where the user would be able to set an API key from the front end, which I decided to store in the .env file and I stored the model chosen and the model provider in a separate SQL database (because I didn't wanna have to deal with encrypting the API key). I also had to add a way for it to be able to retry the API call to the LLM multiple times just in case it ran into any problems (Ex// the output wasn't in JSON format like it was supposed to be)

### Task 2:

I had a pretty good start on this task last week so thankfully it wasn't too difficult for me to finish up. I mostly just implemented the logging of the LLM reponses to analyze later. The most important thing to do was to make sure that everything reset after each iteration of the ablation study. 

### Task 3:

The code has been a little bit of a mess lately because of my tendency to leave TODOs and print statements everywhere. So a lot of this task has been resolving TODOs that I've left behind with some taking a surprisingly long amount of time. One of the biggest sub-task has been optimizing the way that I did the logging. The way I initially implemented it was needlessly complex and probably really prone to bugs. I did it in a way where the logs where initialized somewhere far away from where the logs were actually updated. After some thinking, I realized that I could just initialize the log in the updating function if I just did a check to see whether or not a table already existed. I also briefly started writing documentation for the newly implemented functions



## Results

### Task 1:

There was a lot of trial and error involved in getting it to run but eventually, I was able to get the LLM spitting out the action plan in proper JSON format. There are likely a couple of areas I can make the prompts better, but I plan on doing this once all of the datasets for the ablation study are fully set up.


### Task 2:
Ablation study now runs, just need to find a selection of datasets to run the ablation study on.


### Task 3:
I still have quite a bit more TODOs to get through and also lots more documentation to write. I also realized that I have not updated the DEVNOTES.md file of the project once, so I plan on updating that next week.


## Notes


