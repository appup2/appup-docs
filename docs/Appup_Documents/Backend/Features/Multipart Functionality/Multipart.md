**Multipart Functionality:**

We have 3 email service providers(ses,mailgun,sendgrid) which we are
using now. Through all these providers mails can be sent along with
attachments, but this was previously restricted to download files from
Amazon S3 directly and send them as attachments.

Undertow server was not accepting files coming from third
party.Multipart file attachment support was not present previously, but
now with the new release multipart can be used to send emails along with
attachments.

**Test Scenarios:**

1.  Design Send Grid Attachment node.

2.  Use Setvar or Setvar multi node to which {{request.body}} is sent as
    > input.

3.  Provide the output variable

4.  Now in Send Grid Attachment node, use the above provided output
    > variables in the place of ‘Map Data Key’.

5.  In the place of ‘File Name’, enter the name of the file with which
    > attachment has to be sent.

6.  Use the post calls to upload the documents to {{request.body}}

7.  And the Content-type used here in post call is ‘multipart/mixed’.

8.  When a valid rest call is provided with above inputs,
    > {{request.body}} should accept the files that are being sent to it
    > and mail has to be received along with these attachments.

**Screenshots:**


![Components1](../../../assets/Features_images/multipart/image1.png)


![Components2](../../../assets/Features_images/multipart/image2.png)


![Components3](../../../assets/Features_images/multipart/image3.png)


![Components4](../../../assets/Features_images/multipart/image4.png)


**Postman Collection:**

https://www.getpostman.com/collections/21011a70ee5ab8a40d10
