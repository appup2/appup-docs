**FUNCTIONALITY**:

--------------------------

ActiveMQ is an open source,multi-protocol,java-based messaging server.
This solution receives the messages from Producers, enqueues them and
distributes them to all consumers.

Here we have two workflow nodes implemented

1)ActiveMQ Producer

2)ActiveMQ Consumer

3)ActiveMQ Job Delete

For Scheduling related document, please refer the below link:

[*https://activemq.apache.org/delay-and-schedule-message-delivery*](https://activemq.apache.org/delay-and-schedule-message-delivery)

**Scenarios:**

**----------------**

1)Install ActiveMQ plugin.(Please coordinate with devops to get it
installed and get the Broker URL).

2)Configure ActiveMQ Producer node

3)Configure ActiveMQ Consumer node

4)Publish the app

5)Check the message actions in ActiveMQ home page.1)ActiveMQ Producer:
Messages are sent to consumers using this node.

Below are the different fields present in ActiveMQ Producer node:

a)Topic: When you publish a message it goes to all the subscribers who
are interested - so zero to many subscribers will receive a copy of the
message

b)Queue: A single message will be received by exactly one consumer. If
there are no consumers available at the time the message is sent it will
be kept until a consumer is available that can process the message

c)Destination: The messages are sent and received or stored in activemq
using the destination name.

d)Persistent Mode: This is the default delivery mode, messages are
persisted to disk/database so that they will survive a broker restart

e)Non-persistent Mode: Here in non-persistent delivery, if you kill a
broker then you will lose all in-transit messages.

f)Async Sends: To stream messages to the broker as fast as possible when
you are using persistent messages set it to True.

g)Job Id: Add the Job Id in messages to delete the Queues or Topics
added.

Please check the below screenshots for reference:


