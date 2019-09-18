**Publish Asynchronous**

**Description:**

Previously complete publish process was in a synchronous way. Step by
step we are doing creating config.json and then app.js then log4j.xml
and then storing the deployment into kubernetes. This complete process
will take more time like 30sec.

Now we are implementing publish asynchronous for this creating SNS event
to upload config.json into s3 bucket parallely another SNS event was
created to upload app.js into s3. So in publish asynchronous it is
taking less than 2sec to deploy into kubernetes.

Based on kubernetes speed we will get response for our published url.

**Example To Test:**

Create a sample app for testing and do publish that app and hit the
published url along with “\_appup/\_version”.

You will get an information like cloud id , app name, version and docker
image.

{"CLOUD\_ID":"863","APP\_NAME":"restdynamic","VERSION":"qa-applet-0-j75-04010727172019","DI\_TAG":"applet-0-j75"}

**Success Test Cases:**

1.  Test Case-I:

-   Created an app and published it will display the output.

-   Rename the app and publish.

-   Again hit previously published url (before edit).

-   It has to show an error message like “HTTP ERROR 404”.

1.  Test Case-II:

-   Copy the app publish the url

-   Rename the copied app and publish the url.

-   The published url before rename will get an error message

1.  Test Case -III:

-   Duplicate the app and publish the url

-   Rename the duplicate app and publish the url.

-   Hit both the urls the published url before name will get an error
    > message.

1.  Test Case-IV:

-   Share the app to different account. Publish the url.

-   Rename the shared app and publish the url.

-   Hit both the urls. The published url before rename will get an error
    > message.

1.  Test Case-V:

-   Set one app as default app.

-   Publish the url.

-   Hit the published url and change app name as default

-   For both the urls it has to show an output response.

1.  Test Case-VI:

-   Copy the app to different cloud and do the edit app , copy app,
    > duplicate app and share app.

1.  Test Case-VII:

-   Copy the app from the marketplace and do the edit, copy, duplicate
    > and share app.

1.  Test Case-VIII:

-   Delete the app hit the published url before delete. It has to show
    > an error message.

1.  Test Case-IX:

-   Log level publish.

-   Enable log for a cloud which is there at cloud level settings.

-   Publish an app and hit the published url.

-   Inspect and get “**X-APPUP-REQ-ID “** code from networks**.**

-   Go to the logs for that published app and place that copied Request
    > ID and also provide number of records per page and page number
    > then submit.

-   It has to show log information.

**Failure Test Cases:**

1.  Test Case-IX:

-   Create a custom cloud with the help of devops team and publish an
    > app in custom cloud. As of now publish for custom cloud is not
    > working there an issue with devops.

**Publish Status:**

To check the status of the publish.

1.  Press the “Publish Status” before publishing an app.

> It will show an error and status as failure.
>
> [*https://snag.gy/zXjFkA.jpg*](https://snag.gy/zXjFkA.jpg)
>
> image

1.  When ever it will take some time or having any issue to fetch
    > information from kubernetes it will show as “ Unable to fetch pods
    > status”.

https://snag.gy/zXjFkA.jpg

-   [*https://snag.gy/ZlRQy0.jpg*](https://snag.gy/ZlRQy0.jpg)

> image

2\. First do publish and then hit the publish status button. It will
display message as “Running”.

-   [*https://snag.gy/NknZrt.jpg*](https://snag.gy/NknZrt.jpg)

-   image

3\. When ever it will take some time to fetch information from kubernetes
it will show as pending and status as success.

-   [*https://snag.gy/bN8uqA.jpg*](https://snag.gy/bN8uqA.jpg)

-   image


