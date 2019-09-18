**Reporting - Marketplace App**

**Functionality:**

Reporting app basic functionality is to let the user send the emails
which contain certain data which is derived after executing a SQL
statement. Once the SQL query gets executed data gets fetched and based
on the template id we provided, the report template is also fetched. Now
once the cron app receives all this information, based on the cron
expressions we provide report gets generated and mail is sent to the
user mail list accordingly.

**Technical Details:**

W1(DB Details): A REST call to let the user give DB connection
information. In response, we will send the connection id to the User.

W2(Template): A REST call to let the user send the HTML template with
handle bar’s or FTL, in response to this we will send the template id.

W3(Report Info): A REST call to let the user submit the SQL statement to
execute against the DB, input params are

1.  DB ConnectionId.

2.  SQL Stmt to execute

3.  List of user objects to which the email has to be sent to.

example: \[ {
email:”[*something@nodomain.com*](mailto:something@nodomain.com)”,
fullName:”My full name”, attribute1: “attributeValue1”, attribute2:
“attributeValue2”}\]

1.  HTML template Id using which the email will be sent.

2.  CRON expression and CRON App Url which says when the email should be
    > sent.

3.  example : \* \* \* \* \* (for every minute)

W4(Generate Report): Create the email using HTML template and the
following data for each email recipient.

1.  The data that is passed by the user (Full name, attribute 1,
    > attribute 2)

2.  And the data that is received after executing the SQL stmt.

3.  It is expected that the HTML template will have complete use of
    > handlebars or FTL template which can loop through SQL result set
    > and create the table.

W5(Send Email): It should invoke from generating report and trigger
mail.

**PostMan Collections:**

[***https://www.getpostman.com/collections/d1b82bc07d478502c75b***](https://www.getpostman.com/collections/d1b82bc07d478502c75b)

**Videos:**

[***https://drive.google.com/file/d/1ONuq5GAFxxsBc7ILN5Yc5e2-BiznzuKp/view***](https://drive.google.com/file/d/1ONuq5GAFxxsBc7ILN5Yc5e2-BiznzuKp/view)

**Login Details:**

**Domain:** qa.appup.com

**Username:**
[*kalagarla.venky@gmail.com*](mailto:kalagarla.venky@gmail.com)

**Password:** Captain@07

**Cloud:** marketplace

**App:** reporting-app
