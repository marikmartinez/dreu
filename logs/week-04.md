# Week 4

**Dates:** 07-09 to 07-16

## Goals
- Task 1: Debug some aspects of the system (bugs relating to column types)
- Task 2: Start implementing user log

## Approach and Implementation

### Task 1:
I was running into bugs where my summary statistics calculation functions in the DataProfile class were giving me errors because of the way column types were being determined. For example, I was expecting is\numeric to only give me True if the column was like actually numeric types but it would actually try to see even if string values could be numeric then label the entire column whatever the majority of the data points were. This is why I was running into errors where my functions would try to calculate the max and other numeric summary stats of columns where there were several non-numeric values.

In the codebase, I discovered several different duplicate implementations of functions relating to column types (functions like is\_categorical or is\_numeric and although they _should've_ done the same thing, they didn't. I wanted to kill two birds with one stone by also fixing this problem. Unfortunately, even after hours and hours of trying to merge the different implementations into one, I kept running into even more issues. 

### Task 2:
- I started to implement the user log though I did run into a few problems. Due to my unfamiliarity with React, after trying to figure out how to implement the logger in the front-end, I decided to instead implement it in the back-end.



## Results
### Task 1:
Eventually, this problem took too long and was distracting me from making good progress on my project and I decided to revert everything back and focus on fixing the bug with the summary stat calculation.

### Task 2:
I ran into a lot of bugs as I was doing this and wasn't quite able to finish but I made a lot of progress with this task. 


## Notes


