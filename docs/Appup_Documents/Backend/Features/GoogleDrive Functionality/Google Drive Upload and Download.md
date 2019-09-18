**Google Drive Upload and Download**

Appup is providing a feasibility to upload any file to google drive and
to download any file from google drive.

For this two workflow nodes were provided.

1)Google Drive File Upload

2)Google Drive File Download

As of now we are allowing to download file from amazon s3 also and then
upload it to google drive.Or else we can check it be downloading file
from google drive file download and upload it to google drive.

**Configuration of Workflows:**

In order to get the access to google API we should get a publish key,
secret key. We have to provide this information for google oauth plugin.

Please check the site:
[*https://developers.google.com/oauthplayground/*](https://developers.google.com/oauthplayground/)

After installing the google oauth plugin with valid credentials,using
oAuth token step get the access token details.

**Technical Details:**

**W1(Upload and Download): **

-   This workflow should download a file from google drive using google
    > drive File Download step

-   In OAuth Token step we have to use Google OAuth plugin and
    > parameters.

-   S3 File upload with Decode step is used here to upload a downloaded
    > file into an s3 bucket.

**W2(oAuth):**

-   Step used for this workflow is OAuth. In this step, we provide a
    > redirect URL as publish URL along with google drive file download
    > token trigger expression.

Before running publish URL along with google drive file download trigger
expression we have to add redirect URL which we provided in W2 in Google
account.

**Video Links:**

[***https://drive.google.com/file/d/1SJDWyC4oLLVhZSWL39RXYdWx4qfIAZEG/view***](https://drive.google.com/file/d/1SJDWyC4oLLVhZSWL39RXYdWx4qfIAZEG/view)
