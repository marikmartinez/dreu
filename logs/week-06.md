# Week 6

**Dates:** 07-24 to 07-30

## Goals
- Task 1: Plan out what variables to test
- Task 2: Figure out exactly how to evaluate the LLM
- Task 3: Continue implementing functions for LLM
- Task 4: Continue writing code for ablation study


## Approach and Implementation

### Task 1:
- My mentor pointed out that although I had many ideas of all of the variables I could test, there was likely a limit to how many I could realistically test in my ablation study before the end of the program. He suggested that I narrowed down the variables to those that I found most interesting.

### Task 2:
- Evaluating the LLM would be somewhat difficult as "good" performance doesn't necesarily mean a final dataset with no errors. The LLM may (or may not) be influenced by what the user chooses to do and whether or not the user accepts their suggestions. Therefore, how clean the dataset is shouldn't be the only metric that we take into account.

### Task 3:
- This took (and still is) taking a long time as it includes carefully writing prompts so that they're clear for the llm as well as structuring the code and each individual prompt to the llm so that they will all run properly together.

### Task 4:
- I have to create an ablation study that doesn't actually run the frontend because I don't wan't to be the one actually doing it so I don't have to do it manually. I ran into a lot of problems with actually starting to set this up because the flask functions weren't separated from their logic meaning that instead of being able to call each function directly, I have to call it through a flask api call. I did consider changing the functions so the logic was separate but I've gotten sidetracked enough throughout this project and I really wanted to stay on task. This is definitely a task for the future though!


## Results
### Task 1:
- Gonna simplify my ablation study by only seeing if having / not having the following will have a significant impact on the final dataset:
    - Action log (full, n latest actions)
    - Data profile
    - Error log
    - Full dataset

### Task 2:
- Evaluation:
    - Final dataset: num rows total vs initial rows, num rows w errors vs initial rows w errors, did any rows get new errors?
    - LLM actions: num actions taken, num invalid actions taken, num of actions where it acts on a row with an error, num of redundant / unnecesary actions.


### Task 3:
- Finished this task but I need to actually test everything. I'm assuming that I'll have loads of bugs to go through and fix next week.

### Task 4:
- Good start on ablation study code.




## Notes


