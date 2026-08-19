# Week 8

**Dates:** 08-06 to 08-13

## Goals
- Task 1: Pull request existing code
- Task 2: Find clean datasets of differing sizes
- Task 3: Start script to turn clean datasets into clean ones
- Task 4: Figure out how to avoid being rate limited


## Approach and Implementation

### Task 1: Pull request existing code

I fell a bit behind on commiting my code, so I commited all of it into separate commits, then I did a pull request of each of my branches.

### Task 2: Find clean datasets of differing sizes

For the ablation study, I need to evaluate the performance of the LLM accross a variety of datasets, the most important thing to vary on being size because of LLM context windows. I want to be able to see how the size of the dataset affects LLM response because ideally, the system should provide good actions, regardless of the size of the dataset.

I looked for clean datasets because I plan on "dirtying" them artificially with a script and comparing the clean dataset with the dataset cleaned by the LLM.

The goal was to have one clean dataset of each size:
- Small: ~100-1000 rows
- Medium: ~1000-10,000 rows
- Large: 10,000 > rows

### Task 3: Start creating script to turn clean datasets into clean ones

This script ("create\_dirty\_dataset.py") is supposed to create errors (specifically errors that can be detected by the system like mismatch, missing, anomaly and incomplete) in a clean dataset for the LLM to clean later on.

Each type of error can make up a percentage of the database and each type of error is supposed to be present in each database.

I initially had a hard time trying to figure out how I would randomly select which data points to put the errors in, but the approach that I ended up going with was making a large list of all possible combinations of row id and column name, then for each error, randomly choosing n rows to apply the specific error to, then removing those chosen rows from the list of all possible combinations (because you can only have one error per position).


### Task 4: Figure out how to avoid being rate limited

While doing a run of the ablation study on a dummy dataset (a small, synthetic dataset that I wrote by hand) and on an OpenAI's 120b open source model using free Groq API credits, I noticed that after a certain point, my requests would start failing because I had exceeded my rate limit. This was something I failed to take into account earlier, but I needed to handle it to avoid having the system crash on me.

After some research, I found the pyrate\_limiter package, which allows me to define a Limiter object. It was a bit tricky implementing it despite the function already implemented for me.


## Results

### Task 1: Pull request existing code

Pull requests are up, now just waiting for mentor approval

### Task 2: Find clean datasets of differing sizes

I found a handful of datasets of varying sizes (in terms of rows). However, when shown to my mentor, he brought to my attention that the number of columns also mattered a lot when determining how large a dataset really is. In addition, he also pointed out that 10,000 rows in a dataset isn't very large.

I expanded my list to include a much larger dataset (100,000 rows) and modified my list to take the number of columns into account.

### Task 3: Start creating script to turn clean datasets into clean ones

I got most of the code done for this script, but there are some finishing touches I need to implement next week to get it running the way it should be.

### Task 4: Figure out how to avoid being rate limited

Added rate limiter to requests to LLM.


## Notes
Did not meet with mentor this week due to him being on holiday, but I updated him on my progress through Slack.


