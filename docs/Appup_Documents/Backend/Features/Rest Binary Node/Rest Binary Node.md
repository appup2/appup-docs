**Functionality**

**-------------------**

Previously there is no support for binary file to be sent using REST
call. Now binary file option is been supported using REST.

Tested by using different file formats of images,text,json.

**Rest Binary Node:**

**----------------------------------**

1)Data Key - This will define which key we are passing through binary
option.

2)Data Key Content-type - To define the content type of key we are
passing.ex: multipart/mixed.

3)Headers Content-type - Request content type

4)Body parameters can also be passed under Body section of the
node.Key,Value,Type(content-type of the value being passed) fields are
present.

Ex: Type: image/jpeg, text/csv

5)Connection, read timeout has to provided in order to connect and fetch
the response from rest url to overcome Timeout exception.

**Worked Postman Link:**

**-------------------------------**

[***https://www.getpostman.com/collections/d89bcb6198527c367c98***](https://www.getpostman.com/collections/d89bcb6198527c367c98)

Please check the below screenshots for reference.

![](media/image9.png){width="6.5in" height="3.6527777777777777in"}

![](media/image2.png){width="6.5in" height="3.6527777777777777in"}

![](media/image1.png){width="6.5in" height="3.6527777777777777in"}

![](media/image3.png){width="6.5in" height="3.6527777777777777in"}

![](media/image6.png){width="6.5in" height="3.6527777777777777in"}

![](media/image5.png){width="6.5in" height="3.6527777777777777in"}

![](media/image8.png){width="6.5in" height="3.6527777777777777in"}

![](media/image4.png){width="6.5in" height="3.6527777777777777in"}

![](media/image7.png){width="6.5in" height="3.6527777777777777in"}
