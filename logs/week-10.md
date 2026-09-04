# Week 10

**Dates:** 08-22 to 08-29

## Goals
- Task 1: Fix (many more) bugs in ablation study
- Task 2: Process the results from ablation study
- Task 3: Write paper

## Approach and Implementation

### Task 1:
As I moved on to other tasks, a lot more bugs were showing up in my ablation study that weren't super obvious. For example, bugs that had to do with incorrect / unexpected results rather than bugs that directly caused errors that crashed the script. These were a lot trickier to find and therefore were a lot harder to fix. I ran into many bugs throughout this last week of my project and had to rerun my ablation study more times than I would like to admit! For most of this week, most of my paper was completed apart from the Results and Discussion sections because I had to keep rerunning the ablation study script over and over again because of some new bug I had found. This really slowed down my completion of my paper unfortunately. 

Here are some bugs that I ran into:
- ColumnType bug: the column types class only detects two types: numeric and categorical. I ran into errors with error detection one error type is "incomplete", which is a categorical value that occurs very rarely (< 3 times). When text columns are being counted as categorical and they're something like user names, many data points will be flagged as having "incomplete" errors because the column is being incorrectly classified as a categorical column. When I talked to my mentor about this, he mentioned that some student had already implemented a more detailed version of the ColumnType class that handles this in a different branch from a while back. Merging it in would take a long time to resolve and also re-implementing it would also take a really long time to do. I opted for a TEMPORARY hacky solution of just labeling which columns were text columns, id columns, etc. to avoid inaccurate anomaly detection.

- LLM deleting the ID col:  Despite the prompt telling the LLM to not delete the ID column multiple times, it would sometimes still decide to do it (probably because it's quite a small model). This was problematic because that column is how the LLM determines which row to delete and when deleted, a new ID column is automatically recreated by the Buckaroo system, which no longer aligns with the row ids that the LLM previously knew. I had to fix this by adding a bunch of checks to make sure that the ID column wouldn't be deleted.

- Invalid actions: Initially, I only logged action status as valid or invalid actions. However I ran into this issue where some rows and columns defined by the LLM were invalid and caused the action to quit early. So even though  the action was partially completed, because it ran into some invalid positions, it would quit out of the action early and still be counted as a fully invalid action despite it actually doing something. The quickest fix was to add another action status which was partially invalid which involved separating the valid positions and the invalid positions, performing the action on the valid positions and if the invalid actions list was empty, it would count it was a partially invalid action. Only if all of the positions specified by the LLM were invalid would an action be counted as a fully invalid action.



### Task 2:
- In order to show my results in a way that wasn't incredibly annoying to look at in my paper, I had to find a way to combine my results. Currently, my evaluation scripts were outputting the individual results of my ablation study into different files (ex// results for config1 and dataset1 go into file1, results for config2 and dataset1 go into file2, etc.). I had to put these results together and this is crucial for converting the actual result values into values that made sense (counts to percentages), something I didn't think about before. So, I made a script to combine all of the results of each run in the ablation study into one and calculated the raw evaluation metrics for all of them.

- The results that I got from my ablation study were raw counts, which I needed to convert to percentages so they could be easily understandable in my tables in the paper. I made another script for this task and used the results from the previous script to put the numbers into percentages and also to output it into latex table format to minimize manually inputting the values myself.

### Task 3:
- The task of writing everything else in the paper apart from the Discussion and Results sections was pretty straightforward. As mentioned in Task 2, it took me a while to get to writing those two sections because I had to keep rerunning the ablation study. However, once I got that part actually completed, although the Discussion and Results took quite a bit longer to write than the rest of the paper, I was able to get it completed without too many problems.


## Results

### Task 1:
This task took very very very long to complete but I thankfully eventually fixed all of the bugs that were causing me problems and were creating incorrect / inaccurate results.

### Task 2:
This task was completed fairly easily but it did involve quite a bit of trial and error as the two scripts interacted with each other and if one script was missing something, the other wouldn't behave properly.


### Task 3:
Task completed successfully.

## Notes
Met with mentor over Zoom on 08-24 and 08-28.


