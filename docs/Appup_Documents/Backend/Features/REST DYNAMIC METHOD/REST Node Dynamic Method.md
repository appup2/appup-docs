**SIMPLE REST DYNAMIC METHOD**

**Functionality: **

1.  A REST API defines a set of functions where developers can perform
    > requests and receive responses via HTTP protocol such as GET,POST,
    > PUT and DELETE.

2.  In rest dynamic step we can pass the parameters and the values
    > dynamically through a step.

**Technical Details: **

**W1(testing): **

1.  In this workflow we are providing setvar along with send step to
    > give this publish url along with trigger expression in simple rest
    > dynamic method.

2.  Create a trigger for this with POST or GET or DELETE or PUSH HTTP
    > protocols.

**W2(rest dynamic method): **

1.  In this workflow we will use simple rest dynamic method along with
    > send step.

2.  In this step we will provide url as testing workflow publish url
    > along with trigger expression and method as which we have given in
    > testing trigger expression.

3.  Method type in both the trigger expression must be same to test.

**w3(rest dynamic): **

1.  In this workflow we are testing RawBody functionality for Rest Step
    > With Dynamic Methods by taking sendgrid webhook url.

2.  Url-
    > [*https://api.sendgrid.com/v3/user/webhooks/event/settings*](https://api.sendgrid.com/v3/user/webhooks/event/settings)

3.  Method type - Get

4.  Headers - Authorization key for sendgrid

    a.  Key - Authorization

    b.  Value -{{request,headers.&lt;parameter&gt;}} or

    c.  Value - Bearer
        > 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

5.  RawBody - send grid raw body fields in json format.

> {
>
> "bounce": true,
>
> "click": true,
>
> "deferred": true,
>
> "delivered": true,
>
> "dropped": false,
>
> "enabled": true,
>
> "group\_resubscribe": true,
>
> "group\_unsubscribe": true,
>
> "open": true,
>
> "processed": true,
>
> "spam\_report": true,
>
> "unsubscribe": true,
>
> "url":"[*www.google.com*](http://www.google.com)"
>
> }

5\. More Settings: result

**Screenshots:**

**Workflow 3 (Rest Step)**

1.  In postman we have to provide Authorization value by using key as
    > value in headers

2.  [*https://snag.gy/5HcMgt.jpg*](https://snag.gy/5HcMgt.jpg)

![](media/image4.png){width="6.5in" height="3.6527777777777777in"}

Here output will be your raw body

[*https://snag.gy/adnN1h.jpg*](https://snag.gy/adnN1h.jpg)

![](media/image3.png){width="6.104166666666667in"
height="2.8958333333333335in"}

1.  We can find this node in Utilities.

2.  [*https://snag.gy/hj8pQ9.jpg*](https://snag.gy/hj8pQ9.jpg)

![](media/image2.png){width="5.713542213473316in" height="3.0in"}

1.  Step image -
    > [*https://snag.gy/7wM9te.jpg*](https://snag.gy/7wM9te.jpg)

![](media/image1.png){width="6.5in" height="3.401042213473316in"}

1.  We can provide token values in headers by using key as Authorization
    > and also we can send value dynamically by using
    > {{request.body.&lt;value&gt;}}

2.  [*https://snag.gy/zY6Z1N.jpg*](https://snag.gy/zY6Z1N.jpg)

![](media/image5.png){width="6.5in" height="3.6527777777777777in"}

**Postman Collections: **

https://www.getpostman.com/collections/56a3f31c12aca5318d31

**Credentials:**

W1,W2

Url: qa.appup.com

Username:
[*saradavani.koppisetty@500apps.com*](mailto:saradavani.koppisetty@500apps.com)

Password: 102728

cloudName: ertg

Appname: restdynamicmethod

W3

Url : our.appup.com

Username : [*v56@yopmail.com*](mailto:v56@yopmail.com)

Password : 123456

Cloud Name: v56

App name : rest dynamic method.
