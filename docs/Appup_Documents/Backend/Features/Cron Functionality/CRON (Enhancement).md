**CRON (Enhancement)**

**Functionality:**

-   Cron app is actually used to generate an event based on the time
    > interval which we provide in the form of a cron expression.

-   When a workflow event is associated with the cron expression and
    > published, an event occurs for every time interval we specified.

-   For example, if we provide the expression as **0 \* \* ? \* \***(for
    > ref. [*https://crontab.guru/*](https://crontab.guru/)) then event
    > gets triggered for every one minute.

-   No.of execution times is another feature that is added which
    > actually defines how many times event should execute.

**Technical Details:**

Schedule CRON job with different expressions for performing an action in
the scheduled time intervals.\
\
W1 (Schedule Cron):\
This workflow should send a mail with day and time with below different
trigger expressions\
\
Trigger Expression 1 - Minute - 0 \* \* ? \* \*

**Screenshot Link:**



Once hit the published url it will send mail for every one minute.

Number of execution times is tested through testcron table in reports
schema from mysql workbench.

Screenshot

//image

In the above screen shot.

1.  ID - auto generation key

2.  CRON\_EXP - cron expression for time intervals.

3.  RUN\_TIME - Runtime is the server run time. Once we enable the cron
    > expression runtime will be updated. Initially runtime will be
    > empty.

4.  JOB\_DATA - In job data we pass publishes url, method type and email
    > address.{"args":"{}","url":"[*https://generatereport.appup.cloud/sendmail/email","method":"post","form":"{email:saradavani.42@gmail.com}","headers*](https://generatereport.appup.cloud/sendmail/email%22,%22method%22:%22post%22,%22form%22:%22%7Bemail:saradavani.42@gmail.com%7D%22,%22headers)":"{}"}

5.  STATUS - Initially STATUS is NULL.Ready - Once RUN\_TIME is updated
    > then STATUS is changed to ready

> Inprogress - If RUN\_TIME is less than CURRENT\_TIME then the status
> will be in progress.
>
> Locked -
>
> Done - once the mail sent to the respective email then the status
> changes to done.

1.  BATCH\_ID

2.  NAME

3.  EXECUTION\_TIME - Here we will set number of execution times for
    > cron jobs.

> Example: EXECUTION\_TIME - 4 and CRON\_EXP - 0 \*/10 \* ? \* \*
>
> It will send four emails for every 10 minutes time interval.

Credentials:

Url :
[*https://our.appup.com/\#/home/cloud*](https://our.appup.com/#/home/cloud)

Username /password : [*v56@yopmail.com*](mailto:v56@yopmail.com) /
123456

Cloud / App : 58 /cron
