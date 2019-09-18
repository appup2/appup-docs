**CRON - Marketplace App **

**Functionality:**

-   Cron app is actually used to generate an event based on the time
    > interval which we provide in the form of a cron expression.

-   When a workflow event is associated with the cron expression and
    > published, an event occurs for every time interval we specified.

-   For example, if we provide the expression as \* \* \* \* \*(for ref.
    > [*https://www.freeformatter.com/cron-expression-generator-quartz.html*](https://www.freeformatter.com/cron-expression-generator-quartz.html))
    > then event gets triggered for every one minute.

-   No.of execution times is the new feature that is added in this
    > enhancement which actually defines how many times event should
    > execute.

**Technical Details:**

Schedule CRON job with different expressions for performing an action in
the scheduled time intervals.\
\
W1 (Schedule Cron):\
This workflow should send a mail with day and time with below different
trigger expressions\
\
Trigger Expression 1 - Minute\
Trigger Expression 2 - Hour\
Trigger Expression 3- Daily\
Trigger Expression 4- Weekly\
Trigger Expression 5- Monthly\
Trigger Expression 6- Yearly

**Screenshot Links:**



**Cron Frontend:**

Few pages were developed through which cron job data can be entered and
saved fron frontend side.

Cron can be scheduled by adding the cron job data.

In schedule cron screen click on ‘Add Cron’. Enter the details that are
required.

Provide the cron expression and cron job data.Format for cron job data
is as follows:

Syntax:

{"args":"{}","headers":"{}","method":"POST","form":"{}","url":"RESTURL"}

//image

Different operations which we can perform are create cron,edit cron and
delete cron.

//image

**Video Link:**

[***https://drive.google.com/file/d/1kQTlsh4lZrQ720HcetMxbuVuoDjOJWfP/view***](https://drive.google.com/file/d/1kQTlsh4lZrQ720HcetMxbuVuoDjOJWfP/view)

[***https://drive.google.com/file/d/1qPj5tVSSKmQ5wjzu-bMFcSz93qQ7a\_ds/view***](https://drive.google.com/file/d/1qPj5tVSSKmQ5wjzu-bMFcSz93qQ7a_ds/view)
