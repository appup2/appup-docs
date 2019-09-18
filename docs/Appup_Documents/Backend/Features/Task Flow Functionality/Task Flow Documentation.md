**https://drive.google.com/drive/u/0/folders/19kxLWONGzQDLLDK4fnO9odm3yvbA7ribTask
Flow Description:**

Task flow node is used to execute tasks in a process based on success
and failure status. As of now, we are providing feasibility to add only
rest calls for execution. Any number of REST calls can be executed using
task flow step.

**Prerequisites:**

1)  Designer micro service should get deployed to your respective cloud
    > (for UI). Please coordinate with DevOps team.

2)  In ‘app properties’ set your endpoint app URL or CNAME URL with key
    > “**app\_url**”.

3)  Install DB plugins and create the below table in your schema details

    a.  **Table Structure:**

> *CREATE TABLE \`schedule\_task\` (*
>
> *\`id\` int(11) NOT NULL AUTO\_INCREMENT,*
>
> *\`task\_id\` varchar(45) DEFAULT NULL,*
>
> *\`task\_type\` varchar(45) DEFAULT NULL,*
>
> *\`task\_payload\` varchar(10000) DEFAULT NULL,*
>
> *\`pre\_task\_payload\` varchar(45000) DEFAULT NULL,*
>
> *\`workflow\_payload\` longblob,*
>
> *\`workflow\_json\` longtext,*
>
> *PRIMARY KEY (\`id\`)*
>
> *);*

**Steps to Follow:**

1)  Designer micro-service has to be deployed and the campaign page
    > needs to create (with CRUD operations) by passing the required
    > task node JSON from the app itself.

2)  Create a backend workflow and fetch the designer JSON from the
    > persistent location and pass the data holding variable to the task
    > flow step, also configure the rest calls related information in
    > the task meta info field.

**Video Links:**

[*https://drive.google.com/file/d/1Caqc\_nVpom0dcvvE2Ho8UalV9157njZi/view*](https://drive.google.com/file/d/1Caqc_nVpom0dcvvE2Ho8UalV9157njZi/view)

**For Designer Node:**

[*https://docs.google.com/document/d/1bhtUWWEF5yr0qlhtLZmfenGG\_Y8SelVHAkbZpo4romA/edit*](https://docs.google.com/document/d/1bhtUWWEF5yr0qlhtLZmfenGG_Y8SelVHAkbZpo4romA/edit)

**Note:**

1\) Task Flow with Wait node and Task Sequence retires requires Cron app
v2(enhancement).

2\) For Cron app v2 upgrade instruction document please coordinate with
Venkatesh.

3\) From this docker image(applet-0-58) we are using Quartz API (v2.3.0).

4\) For Taskflow designer micro service ask the developers to contact the
DevOps team.

5\) Schedule id persisted in workflow map, so that the app developer can
implement unschedule the automation with their user and campaign
context.
