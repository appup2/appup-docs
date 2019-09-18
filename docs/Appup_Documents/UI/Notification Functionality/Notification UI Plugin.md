**Functionality**

-----------------

Notification plugin is used for sending web notifications. Along with
Title and body notification is shown in the browser using this plugin.

**Configuration**

------------------

1)Go to frontend- plugins. Install plugin ‘Notification’ with below
mentioned details.

PLUGIN NAME: AppupNotification

PLUGIN SOURCE :
https://appup-cdn.s3.amazonaws.com/static/Notification.js

2)Once the plugin is installed, create a handler as shown in the video.
One for Notification access which actually asks the permission to the
browser to send the notification.

-   And other handler is created for sending the notification
    > content(Title and Body).

-   Add the Timeout to describe for how much time notification should
    > show up in milliseconds.

3)For testing we called these handlers inside a page.

&lt;div&gt;

&lt;h6&gt;Example to get notification handler &lt;/h6&gt;&lt;br&gt;

&lt;button @click.prevent="start('notiaccess',{})"&gt; Request Access
&lt;/button&gt;

&lt;button @click.prevent="start('NotificationLive',{})"&gt; Send
Notification &lt;/button&gt;

&lt;/div&gt;

4)Publish the application and check the changes.

**Note**: In the browser please change the settings for
Notifications,Popup’s and redirects to ‘Allow’ if applicable

Please check the below screenshots for reference.

![](media/image1.png){width="6.5in" height="3.6527777777777777in"}

![](media/image2.png){width="6.5in" height="3.6527777777777777in"}

![](media/image5.png){width="6.5in" height="3.6527777777777777in"}

![](media/image6.png){width="6.5in" height="3.6527777777777777in"}

![](media/image3.png){width="6.5in" height="3.6527777777777777in"}

![](media/image4.png){width="6.5in" height="3.6527777777777777in"}
