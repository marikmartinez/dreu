# Week 2

**Dates:** 06-25 to 07-02

## Goals
Task 1: Add error checking info into the Data Profile dict / json.
Task 2: Implement the Data Profile table into the SQL database
Task 3: Optimize updating of the error and data profile tables

## Approach and Implementation

### Task 1: Add error checking info into the Data Profile dict / json.
This task was pretty simple and straight forward. All I needed to do was query the error table and create error related information to put for each column in the data profile. I had to do a little bit of research to figure out what error related information would even be useful for the LLM.

### Task 2: Implement the Data Profile table into the SQL database
This task was deceptively difficult. My unfamiliarity with PostgreSQL and SQL in general definitely played a part. Not only that, I had to match exactly how other tables were being made so the code base was consistent. It seemed simple enough, but there were a lot more moving parts involved than I thought. For example, sometimes, I'd think I finished the task and realized that the error table was doing something where the data profile wasn't and it caused them both to behave very differently. After a lot of tries, I had the data profile working in about the same way as the error table (in terms of updating it).


### Task 3: Optimize updating of the error and data profile tables
This task was also deceptively difficult. Mostly because I had somehow introduced a bug during my implementation of the optimization and it was so tiny and silly that t took me forever to catch!!! While debugging though, I found a major bug in the code that significantly affected the behavior of Buckaroo and caused it to behave unexpectedly. My mentor said that I should be able to find the fixed version in one of the branches. However, Task 3 took so long that I never got around to fixing the newly discovered bug, making it a task for next week. After hours putting print statements everywhere, I found my bug and fixed it (I just passed in the variables into a class in the wrong order). The implementation itself was also kind of difficult though as I wanted it to be as efficient as possible and there were so many different ways to optimize it.

The way Buckaroo was updating the error tables and the data profile tables was by updating the __entire table__ after each change the user made, even if it was just a change to one row. This slowed down the system a lot, so we wanted to only update the column names in the error table and the data profile table that were actually affected by the user wrangles. The error tables and data profile tables contain information about each column of data in the main dataset, so I figured that after each wrangle by the user, I would just delete the data in the error table and the data profile table relating to the column(s) that they wrangled. Then, I would pass the wrangled columns through the functions that create the error table and data profile tables and then merge these tables with the existing tables.

I explained my approach to my mentor, who suggested that I do "dirty flagging" instead. I didn't quite realize that the approach he described was all that different to the one I was already doing so I implemented my approach and only after did I realize that the approach he described was a bit different and a lot more efficient. Luckily, I think that the implementation of my approach makes it much easier to implement the "dirty flagging" method my mentor described. I will be implementing this method next week.

## Results
I was able to implement the data profile table, which plays a huge part in the implementation of the AI assistant as it contains a lot of the information needed to give to the LLM. The optimization of the error and data profile tables, though not fully complete, also is a big step in making Buckaroo faster, especially with larger datasets.

## Notes

(No in-person meeting this week due to student's transportation issues and mentor travel)
Met with mentor on 06/26 and 06/30




