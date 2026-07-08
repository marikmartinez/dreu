# DREU Summer 2026: Buckaroo + AI Assistant
Mentor: Dr. Paul Rosen at the University of Utah
Student: Marianne Martinez (University of Hawaii at Hilo & University of Utah)

## Project Overview

Buckaroo is a visual data wrangling 

Though Buckaroo already suggests wrangles to the user, it can be difficult for the user to decide which actions to perform first. Should the user prioritize removing errors from one column or prioritize making sure that all data types are the same in another? There isn't one single right answer to this problem: it depends on what the user's goals are. 

Under the mentorship of Dr. Paul Rosen, I will be incorporating an AI assistant into Buckaroo in order to help the user make wrangling decisions. The AI assistant will be an LLM given information about the user (user goals, user preferences, past user wrangles, etc.), context about the dataset (what the dataset is of, the columns, etc.) and detailed information about the dataset (summary stats, errors, etc.). Using this information, the LLM will create a "wrangling plan" for the user to act on as well as guide them to data points that are interesting.

### Project Goals

#### Week 1
- Get familiar with the code base & with Buckaroo app
    - Calculate summary stats of the dataset and save them to a json
        - Research some summary stats

#### Week 2
- Implement data profile table
    1. Create more summary statistics using the error stats
    2. Put the summary stats into a SQL table

- Optimize updating of data profile and errors table
- Get an idea of what kind of information the LLM might need

#### Week 3
- Fix bugs
    - Fix deletion bug
- Transition from pandas df to SQL queries so that the system can be more efficient
    - Transition data profile class from pandas and SQL to just SQL
    - Transition error detectors from pandas to just SQL (One implementation already in one of the branches)
- In-depth literature review
    - How to prompt the LLM for this task
    - What data to give the LLM
- Start implementing unit tests for data profile functions & other modified functions

#### Week 4
- Start creating user profile(information about the user to give to the LLM)
- Draft of LLM prompt
- 

#### Week 5


#### Week 6
#### Week 7
#### Week 8
#### Week 9
#### Week 10

## Relocation Status

I have relocated to Salt Lake City and meet with Dr. Rosen at the University of Utah at least once a week. We meet once a week virtually over Zoom also.




