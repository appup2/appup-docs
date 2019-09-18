**TASK SEQUENCE**

**Functionality:**

Task sequence app executes multiple sequence of tasks in sequence mode.
All the REST api calls are provided and all the tasks related payload
data is provided in the JSON format.So based on the sequence we provide
all the rest api calls gets executed.

Retries is another feature present in task sequence. For every rest call
we can add these retries. As of now retries concept is applicable only
when we face 500 or above 500 server errors on rest calls.

So once 500 error occurs, based on the retries count api call gets hit
based on the cron time interval set in the backend side.

If the retries count is 5 and at backend side if cron time interval is
set for every 5 minutes then the rest call gets hit for every 5 minutes
total for 5 times.

Within this time if rest call gets executed successfully, it executes
remaining rest calls sequentially.

Even after 5 retries rest call gets failed to execute, then the
remaining rest calls will not execute. Execution stops with the current
rest calls failure status.

**Technical Details:**

Workflow 1(REST\_EMAIL):\
This workflow should send a message to respective mail-id.\
\
Workflow 2(SELECT\_DATA):\
This workflow should get data from DB.\
\
Workflow 3(EMAIL\_CONTENT):\
This workflow should get the email content to sent from DB.\
\
Workflow 4(TASKSEQUENCE\_WORKFLOW)\
This workflow should execute the remaining workflows in a sequence based
on tasks type and url.

**PostMan Collections:**

[***https://www.getpostman.com/collections/c968b0d2e49f1102684c***](https://www.getpostman.com/collections/c968b0d2e49f1102684c)

**Videos:
[*https://drive.google.com/file/d/1RRMHwTv8-M4OySNJzR4gral7RkhfG5z1/view*](https://drive.google.com/file/d/1RRMHwTv8-M4OySNJzR4gral7RkhfG5z1/view)**
