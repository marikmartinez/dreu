# DREU Summer 2026: Buckaroo + AI Assistant
Mentor: Dr. Paul Rosen at the University of Utah
Student: Marianne Martinez (University of Hawaii at Hilo & University of Utah)

## Project Overview

Buckaroo is a visual data wrangling system. The user can select a selection of data and the system will suggest wrangles that the user can perform. Accompanied by the suggestions are informative graphs of what the data will look like after they are performed, allowing the user to directly see how their wrangles will affect their dataset. In addition, the system will also point out certain anomalies that are detected in their dataset.

Though Buckaroo already suggests wrangles to the user, it can be difficult for the user to decide which actions to perform first. Should the user prioritize removing errors from one column or prioritize making sure that all data types are the same in another? There isn't one single right answer to this problem: it depends on what the user's goals are. 

Under the mentorship of Dr. Paul Rosen, I will be incorporating an AI assistant into Buckaroo in order to help the user make wrangling decisions. The AI assistant will be an LLM given information about the user (user goals, user preferences, past user wrangles, etc.), context about the dataset (what the dataset is of, the columns, etc.) and detailed information about the dataset (summary stats, errors, etc.). Using this information, the LLM will create a "wrangling plan" for the user to act on as well as guide them to data points that are interesting with an explanation as to why those specific data points may be of interest to the user.

Original Buckaroo paper: https://arxiv.org/pdf/2507.16073

### Project Goals
_Note_: These project goals are not set in stone and will be adjusted and fleshed out as the program goes on. 

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
- Create user profile(information about the user to give to the LLM)
- Draft of LLM prompt
    - Figure out how LLM will perform actions
    - Draft format that LLM should respond in
- Continue to transition error detectors from pandas df to SQL

#### Week 5
- Start implementing LLM into the system
    - Start implementing functions that LLM can interact with

#### Week 6
- Continue to implement LLM into the system

#### Week 7
- Experiment with different kinds of prompts (based on research)

#### Week 8
- Start writing final report

#### Week 9
#### Week 10

## Relocation Status

I have relocated to Salt Lake City and meet with Dr. Rosen at the University of Utah at least once a week. We meet once a week virtually over Zoom also.




