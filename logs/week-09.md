# Week 9

**Dates:** 08-14 to 08-21

## Goals
- Task 1: Complete "create\_dirty\_dataset.py" script and make bash script to create multiple dirty datasets
- Task 2: Add delay for LLM API calls (to avoid hitting rate limits)
- Task 3: Run ablation study with free model
- Task 4: When ablation study fully functional, use paid model
- Task 5: Make outline for final report
- Task 6: Write evaluation scripts


## Approach and Implementation
### Task 1:
- I added each of the errors to the "create\_dirty\_dataset.py" script and made it so that you can assign a percentage of the data points in the dataset that you want each specific error to make up. I saved the created dirty datasets to their own directory for later use.
    

### Task 2:
- Adding this delay involved using the pyrate package which meant that the implementation wasn't too difficult. However, the free rate limits for the  LLM were really going to slow my project down and I needed to consider spending money for it to run better and faster.

### Task 3:
- This took lots and lots of debugging to get running as I wanted it to. I was running into errors mostly because of silly mistakes that I had made earlier in the implementation process. Eventually, I got it to a state where it wasn't crashing with an error thankfully.

### Task 4:
- Although I wasn't really planning on using a paid model, the ablation study was using much more tokens and requests than I had expected, meaning that I was hitting my daily limits within a very short amount of time. I tried out a couple of gemini's models for the task and eventually settled on their 3.1 flash lite model.

### Task 5:
- I created a very rough outline for my final paper where I outlined each major part of the paper as well as started some of the sections such as the introduction and the methods.

### Task 6:
- This task wasn't too difficult as it just involved calculating some values from the results of my ablation study, but it involved quite a bit of trial and error since I would realize I would be missing something from the ablation study to calculate an evaluation metric so I'd have to make changes to my ablation study to make the calculation actually possible to make.



## Results
### Task 1:
- This task was completed fairly quickly however I realized that I had a pretty big flaw in picking out my "clean datasets" to make "artificially dirty". I had only picked out datasets without the missing errors, completely missing the fact that I also had to check that the datasets didn't contain other errors such as anomaly errors, mismatch errors, etc. So I was making already dirty datasets even more dirty. It was a pretty silly mistake in hindsight and eventually, I just decided to run the ablation study without the "artificially dirty" datasets.

### Task 2:
- I got this running and it was working really well for avoiding the minute rate limits which was very convenient but hte day rate limits were really what were getting in my way after this was implemented. So although this solved one problem, it opened up another which could only be fixed by paying for the model credits.

### Task 3:
- This task took a lot of time as debugging one error would just show another error. A lot of the times, the errors would only show up sometimes because the LLM responses would be different for each ablation study. However, I successfully completed this task in the end.

### Task 4:
- This was a fairly simple taska and it was very easy to get completed.

### Task 5: 
- Because Task 3 took so much time because I kept uncovering bugs in my code, I wasn't able to get as much done on the outline as I had wanted. However, I plan on focusing much more on this task next week.


## Notes
Met with mentor virtually on 08/17 and in-person on 08/19.

