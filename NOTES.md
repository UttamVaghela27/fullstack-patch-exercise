# Notes

## Summary of changes

I fixed two issues in the task tracker.

First, the status filter was not working correctly because the SQL query had incorrect AND/OR grouping. This allowed tasks with other statuses to appear in the results.

Second, changing the search query or status filter did not reset the current page. This could make the application show no results even when matching tasks existed on page 1.

## What I chose not to change

I did not make unrelated UI or backend changes because the exercise is time-boxed and I wanted to keep the patch focused. I also did not change the API contract or database schema.

## Biggest remaining risk

The application performs pagination after loading the filtered results into memory. This may become inefficient as the number of tasks grows because the backend could load many records before returning one page.

## Tools/AI used

I used CHATGPT/AI assistance to inspect the codebase, trace request flow, identify potential bugs, and review the proposed fixes. I manually tested the API and UI before accepting the changes and reviewed the generated code changes myself.
