# Week 3

**Dates:** 07-02 to 07-09
_Note_: Missed Tuesday and Wednesday during the week because some things came up, both of which were made up during the weekend

## Goals
Task 1: Commit and document code to repo.
Task 2: Find bug fix to the "deletes whole selection" bug instead of deleting the rows with errors and also look for SQL implementations of error detectors in other branches.
Task 3: Transition data profile class & error detectors from pandas data frames to just SQL queries
Task 4: Do a literature review on what information should be given to the LLM and what good prompts for it are.

## Approach and Implementation
### Task 1: Commit and document code to repo.
dreu\_ai branch of Buckaroo is now up to date. New changes are being committed regularly.

### Task 2: Find bug fix to the "deletes whole selection" bug instead of deleting the rows with errors and also look for SQL implementations of error detectors in other branches.
Deletion bug was fixed. Just modified the SQL query so the expected behavior happens. Another bug, the imputation bug, was found and also fixed.

The SQL implementations were found in another branch but the branch is 112 commits behind the main branch. Mentor said that if it's too much hassle to implement, maybe it's not worth doing. I started to catch up the branch but there were so many merge conflicts, it wasn't clear what was still being used and what wasn't. Maybe at some point in the future, I can pick up this task again, but starting to put more work on the main focus of the project is a bigger priority than optimizing the current system.


### Task 3: Transition data profile class & error detectors from pandas data frames to just SQL queries

Transitioned data profile class into SQL queries but as stated in the previous task, transitioning the error detectors is going to have to be a task for another time.


### Task 4: Do a literature review on what information should be given to the LLM and what good prompts for it are.

I searched for what information to give LLM for this specific task but not much could really be found as this task isn't very well researched, especially with LLMs and especially as a task that doesn't involve code generation. I did find one paper that involved using an LLM and using data instances to generate context to use for the LLM prompt which I think I will try as an approach.I also found several good general practices for prompt engineering that I could test out and I could see which one performs the best. 

As for information to actually give the LLM, again, not too much information. A lot of papers don't go into detail on what information to give their models (LLM or just deep learning models) and it seems like a lot of them just give the whole dataset. My mentor and I discussed this approach at the very beginning of the program and both agreed that it seemed very inefficient and that we would give the LLM metadata about the dataset instead. I think I will just try out giving the LLM different kinds of information and figuring out which works best.

## Results
It was a very productive week for me and the literature review will really help with starting to implement this AI assistant. 



## Notes
My mentor and I met on July 6th in person and July 9th on Zoom.



