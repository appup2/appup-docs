**Send Grid Custom Header Email **

**Functionality:**

Send Grid Custom Header Email is used to send an email with/without
attachments by passing custom headers. This can be done by passing Send
Grid API key dynamically.

For this, we have to generate an API key by creating an account on this
[*https://signup.sendgrid.com/*](https://signup.sendgrid.com/) website.

**Test Scenarios for Workflow (Without Attachments) :**

We have to provide the following details into the send grid custom
header email node.

From Name, From Email, To Email, Cc and Bcc, Reply To, Output Variable
and Custom Headers.

//image

//image

Provide API key in Auth Info, Subject and text message in Body fields.

//image

Give a Setvar for the Success and failure state of send grid custom
header email, and connect it to the sendstep to receive the message in
the browser.

//image

**Test Scenarios for Trigger :**

We have to provide the following details in to the Rest trigger to
execute workflow.

Name, Assign to a Category, Method, Expression and What to Execute.
//image

Publish the application and hit the cluster in the browser to receive
the email with custom headers.

**Test Scenarios for Workflow (With Attachments) :**

In s3 file download, we have to provide a File Name, Output Variable,
Bucket Path and s3 plugin.

We have to provide the following details into the send grid custom
header email node and add
attachments.
//image

From Name, From Email, To Email, Cc and Bcc, Reply To, Output Variable,
Attachments and Custom Headers.

//image

//image

Give a Setvar for the Success and failure state of send grid custom
header email, and connect it to the sendstep to receive the message in
the browser.

//image

**Test Scenarios for Trigger :**

We have to provide the following details in to the Rest trigger to
execute workflow.

Name, Assign to a Category, Method, Expression and What to Execute.


Publish the application and hit the cluster in the browser to receive
the email with attachments using custom headers.
