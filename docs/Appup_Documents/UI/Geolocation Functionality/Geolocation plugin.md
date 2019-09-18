**Functionality**

------------------

Geolocation is generally used to identify the location of an
object.Geolocation plugin is developed in order to locate the latitude
and longitude wrt location.

**Configuration**

-------------------

1)Go to frontend- plugins. Install plugin ‘Geolocation’ with below
mentioned details.

PLUGIN NAME: AppupGeolocation

PLUGIN SOURCE :
[*https://appup-cdn.s3.amazonaws.com/static/Geolocation.js*](https://appup-cdn.s3.amazonaws.com/static/Geolocation.js)

2)Once the plugin is installed, create a handler as shown in the video.
We tested the geolocation by using the sample JS code.

function(data,ui)

{

alert("Latitude = "+data.lat);

alert("Longitude = "+data.long);

}

3)For testing we called this handler inside a page.

&lt;div&gt;

&lt;h6&gt;Example to get Geolocation handler &lt;/h6&gt;&lt;br&gt;

&lt;button @click.prevent="start('geolocate',{})"&gt; Get Lat
long&lt;/button&gt;

&lt;/div&gt;

4)Publish the application and check the changes.

**Note**: In the browser please change the settings for
Notifications,Popup’s and redirects to ‘Allow’

Please check the below screenshots for reference.

![](media/image2.png){width="6.5in" height="3.6527777777777777in"}

![](media/image8.png){width="6.5in" height="3.651042213473316in"}

![](media/image9.png){width="6.5in" height="3.6527777777777777in"}

![](media/image7.png){width="6.5in" height="3.6527777777777777in"}

![](media/image5.png){width="6.5in" height="3.6527777777777777in"}

![](media/image4.png){width="6.5in" height="3.6527777777777777in"}

![](media/image1.png){width="6.5in" height="3.6527777777777777in"}

![](media/image3.png){width="6.5in" height="3.6527777777777777in"}

![](media/image6.png){width="6.5in" height="3.6527777777777777in"}
