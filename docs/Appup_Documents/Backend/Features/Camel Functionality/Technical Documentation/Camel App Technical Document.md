**Camel App:**

**Functionality:**

Camel App is used to send emails and upload documents to s3 , creating
pdf ,creating local file and send notification with message body . It
requires uri , headers and body . uri is the one which we want to
perform action need to provide in the form of camel endpoint uri ,
headers is the one which we want to add any header information to uri ,
message is the one which we want to send message body.

**Technical Details:**

Workflow 1:

This workflow will take uri , headers and message and it will process
the action based on the url provided. You can add multiple headers with
separating comma in key and value pairs.

If you want to send email through ses then you have to provide
information like below

uri:
**aws-ses://[*noreply@unscr.me*](mailto:noreply@unscr.me)?region=US\_WEST\_2&accessKey=AKIAJNLQ5LXNMMXCLLMA&secretKey=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&subject=CamelTest&to=apachecamel@yopmail.com**

message: **Hello world**

headers:
CamelAwsSesFrom=[***noreply@unscr.me***](mailto:noreply@unscr.me) ,
CamelAwsSesTo=[***apachecamel@yopmail.com***](mailto:apachecamel@yopmail.com)

If you want to upload document in s3 with given message body through s3
then you have to provide information like below

uri:
aws-s3://appup-bucket?region=US\_EAST\_1&accessKey=AKIAIVJMBGBK4PRJ3SKA&secretKey=RAW(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)

message: **Hello world**

headers: CamelAwsS3Key=test/ghhjj.txt ,
CamelAwsS3BucketName=appup-bucket

**Postman Links:**

**https://www.getpostman.com/collections/80ad03d7e8dbd880d946**

**Video Link:**

[***https://drive.google.com/file/d/1plVF39fbNoHt7r3hGrylbRXNHkvKIqxs/view***](https://drive.google.com/file/d/1plVF39fbNoHt7r3hGrylbRXNHkvKIqxs/view)

[***https://drive.google.com/file/d/1joBKEq2TxQTmjHGRaC7zRHNeyXSMYa98/view***](https://drive.google.com/file/d/1joBKEq2TxQTmjHGRaC7zRHNeyXSMYa98/view)

**Login Details:**

**Domain:** QA

**Username:** camel@yopmail.com

**Password:** 123456

**Cloud:**appupcamel

**App:** camel
