Introduction
============

Notification app will be used as a one-stop point to send notifications
to clients. This notification app is a wrapper around other notification
services like “PubNub”, “Ably” and “Pusher”,”SNS”.

This is required so that the developer has no new learning curve to
complete once he knows how to use this Notification App.

Notifications app will also help to navigate away from existing
notification service without having to worry about a lot of change in
the code.

In the future, the notification application will also load balance the
number of messages to be sent to different notification service
providers based on certain criteria given by users.

### Terminology

Tenant/User: The individual or entity who is using the Notification app
to send messages/notifications.

Developer: The individual who is developing the Notification app

Provider: PubNub, Ably, Pusher,”SNS”

Overview
--------

The Tenant who wishes to use this notification app will first have this
app copied from the 500Apps marketplace to his cloud.

Once he copies the app into his cloud the rest workflows of the
application are exposed along with the UI, after logging in with the
AppupSSO the following are the use cases that will be considered.

Prerequisites:

Plugins:

Install JDBC sessions,MySQL

Designed Workflows:

1)SetSession: This workflow is used to set the session values into the
database. Here we provide user-id, username in order to set the session
values.

2)GetSession: This workflow is used to validate the userid and username
which we provided. If the username exists then a message is shown like
‘User id is existing’. If the user doesn’t exist then the user
information will be stored in a database.

3)Configure: This workflow is used to configure the provider
information.

Inputs that need to be provided here are: Provider name, Provider
related information(api\_key, secret keys etc). It varies depending on
the provider name.

Hereafter providing all the information, an api\_key is generated which
is used to publish the message.

4)Publish: This workflow will publish the message which we provide to
the end user based on the message, channel name,api\_key we provide.

Reference Links:

![Components1](../../assets/Marketplace%20Apps%20Images/NotificationApp/image1.png)


(https://www.ably.io/documentation)

![Components2](../../assets/Marketplace%20Apps%20Images/NotificationApp/image2.png)


(https://www.pubnub.com/docs/java-se-java/api-reference-publish-and-subscribe#publish)

![Components3](../../assets/Marketplace%20Apps%20Images/NotificationApp/image3.png)


(https://pusher.com/docs/client_api_guide/client_events)
