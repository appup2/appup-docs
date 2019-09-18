**MailGun Custom Step**

**Functionality:** It is used to send email to authorized recipients. We
can send an email with a single attachment and also with multiple
attachments to authorized users.

**Technical Details: **

W1(mailgun custom step): This workflow should send an email to the
authorized mail ids which are there in mailgun account.

In this workflow, we are providing an attachment from the s3 bucket.

We can also use box API file download and also onedrive file download
step for attachments.

In this mailgun custom step, we need to provide API key and host as
sandbox name from your mailgun account.

Once we run the published URL in postman it will send an email to
authorized users.

**Reference Links for MailGun:**

1.Create an account in mailgun -
[*https://app.mailgun.com/*](https://app.mailgun.com/)

2.You will receive a link to your email. Please, login through that
link.

3.Click on domains and you can find sandbox account name click on that
sandbox account you can find API key.

4.Use sandbox account name as Host

5.Mailgun account API key as API key in Mailgun Custom Step.

6.To send an email through mailgun we have to add emails in Mailing List
to subscribe to mailgun account.

[*https://snag.gy/5wu4zk.jpg*](https://snag.gy/5wu4zk.jpg)

8.You can only send an email to subscribed mail ids.

**PostMan Collections: **

[*https://www.getpostman.com/collections/8507d13d776eabf21bb4*](https://www.getpostman.com/collections/8507d13d776eabf21bb4)

**Screenshots:**

Create an account in mailgun

[*https://snag.gy/XEGt9q.jpg*](https://snag.gy/XEGt9q.jpg)

![](media/image10.png){width="6.5in" height="3.6527777777777777in"}

It will send an verification link to your mail id.Please login through
that link.

It will ask your mobile verification.Please, provide a valid mobile
number

[*https://snag.gy/w6Jydh.jpg*](https://snag.gy/w6Jydh.jpg)

![](media/image8.png){width="6.640625546806649in"
height="3.720055774278215in"}

Login to mailgun account

[*https://snag.gy/3l5IP6.jpg*](https://snag.gy/3l5IP6.jpg)

![](media/image6.png){width="6.5in" height="3.6527777777777777in"}

Click on Domain for host and apikey

[*https://snag.gy/9zPCQA.jpg*](https://snag.gy/9zPCQA.jpg)

![](media/image11.png){width="6.5in" height="3.6527777777777777in"}

Adding recipients

Click on email validation

[*https://snag.gy/2QsDIv.jpg*](https://snag.gy/2QsDIv.jpg)

![](media/image14.png){width="6.5in" height="3.6527777777777777in"}

click on upgrade it will redirect to a page click on invite new
recipients

[*https://snag.gy/1KVQvP.jpg*](https://snag.gy/1KVQvP.jpg)

![](media/image12.png){width="6.5in" height="3.6527777777777777in"}

[*https://snag.gy/f3Cd6U.jpg*](https://snag.gy/f3Cd6U.jpg)

![](media/image13.png){width="6.5in" height="3.6527777777777777in"}

Add respective emails here

[*https://snag.gy/0jwsp4.jpg*](https://snag.gy/0jwsp4.jpg)

![](media/image9.png){width="6.5in" height="3.6527777777777777in"}

Here your mail is unverified . please login to your email which we added
in maillist

[*https://snag.gy/49A5vd.jpg*](https://snag.gy/49A5vd.jpg)

![](media/image7.png){width="6.5in" height="3.6527777777777777in"}

![](media/image2.png){width="6.5in" height="3.6527777777777777in"}

![](media/image15.png){width="6.5in" height="3.6527777777777777in"}

[*https://snag.gy/v1n90N.jpg*](https://snag.gy/v1n90N.jpg)

Now your mail was verified. You can send mails to this verified mail id
through mailgun custom step.

**Credential:**

Url: our.appup.com

Username: [*v56@yopmail.com*](mailto:v56@yopmail.com)

Password: 123456

Cloud : v56

App: mailgun

Mailgun custom step node:

[*https://snag.gy/e8aksy.jpg*](https://snag.gy/e8aksy.jpg)

![](media/image3.png){width="6.5in" height="3.638888888888889in"}

[*https://snag.gy/IClS6A.jpg*](https://snag.gy/IClS6A.jpg)

![](media/image4.png){width="5.946642607174104in"
height="3.9739588801399823in"}

[*https://snag.gy/8KSMey.jpg*](https://snag.gy/8KSMey.jpg)

![](media/image1.png){width="6.6875in" height="3.1093755468066493in"}

To verify the output run the published url in postman and then verify
your mail.

[*https://snag.gy/QV6DA0.jpg*](https://snag.gy/QV6DA0.jpg)

![](media/image5.png){width="6.5in" height="4.694444444444445in"}
