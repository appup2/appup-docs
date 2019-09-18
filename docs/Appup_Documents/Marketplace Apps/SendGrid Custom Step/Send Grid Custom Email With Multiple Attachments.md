**Send Grid Custom Email With Multiple Attachments**

**Functionality:**

In send grid custom email, send grid custom step is used to send an
email with multiple attachments bypassing Send Grid API key dynamically.

For this, we have to generate an API key by creating an account on this
[*https://signup.sendgrid.com/*](https://signup.sendgrid.com/) website.

Here we are providing attachments using s3 file download step. If we
want to send with multiple attachments we have to use multiple s3 file
download steps.

**Technical Details:**

W1(sendgrid\_custom\_withattachment): This workflow should send an email
with multiple attachments. Here we will use an api key to connect with
sendgrid.We have to provide generated API key in Send Grid Custom Email
step Auth Info.

We have to install s3 plugin for s3 file download.

**Test Scenarios:**

In s3 file download, we have to provide a filename, bucket path, and s3
plugin.

We have to test this send grid custom email by providing input values
like

From(Name),

From(Email),

To Mail,

CC Mail,

BCC Mail.

Subject,

Text.

**PostMan Collection:**

[*https://www.getpostman.com/collections/6ed8839a264e5401367b*](https://www.getpostman.com/collections/6ed8839a264e5401367b)

**Video: **

[*https://drive.google.com/file/d/1PcRS0YgckhmTXe05yoXbLLWwSROXcDvu/view*](https://drive.google.com/file/d/1PcRS0YgckhmTXe05yoXbLLWwSROXcDvu/view)
