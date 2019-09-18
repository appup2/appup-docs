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

![](media/image5.png){width="5.917361111111111in"
height="4.489583333333333in"}

![](media/image8.png){width="5.875in" height="4.729166666666667in"}

Provide API key in Auth Info, Subject and text message in Body fields.

![](media/image10.png){width="5.427083333333333in"
height="3.8854166666666665in"}

Give a Setvar for the Success and failure state of send grid custom
header email, and connect it to the sendstep to receive the message in
the browser.

![](media/image7.png){width="4.853472222222222in"
height="3.6458333333333335in"}

**Test Scenarios for Trigger :**

We have to provide the following details in to the Rest trigger to
execute workflow.

Name, Assign to a Category, Method, Expression and What to Execute.

![](media/image6.png){width="4.514583333333333in"
height="3.338888888888889in"}

Publish the application and hit the cluster in the browser to receive
the email with custom headers.

**Test Scenarios for Workflow (With Attachments) :**

In s3 file download, we have to provide a File Name, Output Variable,
Bucket Path and s3 plugin.

We have to provide the following details into the send grid custom
header email node and add
attachments.![](media/image2.png){width="5.952083333333333in"
height="4.366666666666666in"}

From Name, From Email, To Email, Cc and Bcc, Reply To, Output Variable,
Attachments and Custom Headers.

![](media/image9.png){width="4.676388888888889in"
height="3.4347222222222222in"}

![](media/image4.png){width="5.490277777777778in" height="4.2875in"}

Give a Setvar for the Success and failure state of send grid custom
header email, and connect it to the sendstep to receive the message in
the browser.

![](media/image1.png){width="4.959027777777778in"
height="4.215277777777778in"}

**Test Scenarios for Trigger :**

We have to provide the following details in to the Rest trigger to
execute workflow.

Name, Assign to a Category, Method, Expression and What to Execute.

![](media/image3.png){width="5.011111111111111in"
height="3.7743055555555554in"}

Publish the application and hit the cluster in the browser to receive
the email with attachments using custom headers.
