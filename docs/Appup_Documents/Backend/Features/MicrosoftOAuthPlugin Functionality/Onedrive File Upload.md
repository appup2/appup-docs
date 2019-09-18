**Onedrive File Upload**

**Functionality:** Onedrive file upload is used to upload a downloaded
file from different drives like google drive, s3 bucket, a box account
and upload that downloaded file into one drive by using one drive file
upload.

For this, we have to create an account in Microsoft and Onedrive.

While installing Microsoft oauOAuthugin we have to provide key, secret
key from Microsoft account and scope as Files.ReadWrite.All.

**Technical Details:**

**W1(onedrive file download token): **

-   This workflow should download a file from one drive using Onedrive
    > File Download step

-   In OAuth Token step we have to use Microsoft OAuth plugin and
    > parameters.

-   S3 File upload with Decode step is used here to upload a downloaded
    > file into an s3 bucket.

**W2(onedrive file download filter):**

-   Step used for this workflow is OAuth. In this step, we provide a
    > redirect URL as publish URL along with onedrive file download
    > token trigger expression.

Before running publish URL along with onedrive file download filter
trigger expression we have to add redirect URL which we provided in W2
in Microsoft account.

**Reference Links:**

Create an account in Microsoft:
//image

Login to:
//image

Create an app by clicking add app button and mention your application
name

Once you click on that app you can find application id and click on
generate new password button.

While installing a plugin, use your application id as key and password
as secret, Files.ReadWrite.All as scope.

Onedrive -
//image
→ Goto My OneDrive → to check your uploaded files.

**Output:**

After running the published URL It will redirect to Microsoft account.
Please, provide valid credentials.

Once check your S3 bucket with whatever file you gave in your S3 file
upload with decode step.

**Video:**
[*https://drive.google.com/file/d/1H-bhciqOsKcDIHvPk1k-YKNwnClBqQPi/view*](https://drive.google.com/file/d/1H-bhciqOsKcDIHvPk1k-YKNwnClBqQPi/view)
