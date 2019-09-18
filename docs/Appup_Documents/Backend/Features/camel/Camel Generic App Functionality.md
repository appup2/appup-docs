![](media/image3.png){width="4.390625546806649in"
height="1.8151716972878391in"}

**APP in AppUp**

**What is Apache Camel:**

Apache Camel is an open source Java framework that focuses on making
integration easier and more accessible to developers. In other words, it
helps us to integrate with the other frameworks using some mediation
rules. It joins together messaging start and end points allowing the
transference of messages from different sources to different
destinations.

**Deployment of Camel:**

Need to deploy camel in your cloud for deployment, please coordinate
with DevOps team, once published they will provide the endpoint URL to
which all the input required has to be passed to postman collections to
pass the inputs to camel generic.

Please check the postman collection link and it’s form-data for inputs.

**Camel REST API:**

To achieve this integration camel generic step is used. There are three
main inputs which need to be provided.

1)URI

2)Message

3)Headers

1)**URI**: We pass properties respective to the component with which we
want to integrate. The URI syntax changes for every component.

For example,

SES URI Syntax: aws-ses://from\[?options\]

SNS URI Syntax: aws-sns://topicName\[?options\]

2)**Message**: To support various message exchange patterns like one-way
Event Message and Request-Reply messages Camel uses an Exchange
interface.

3)**Headers**: The Header Expression Language allows you to extract
values of named headers.

Here we enter Headers to the URI. Instead of URI options, it can be
overridden by providing header values.

**Postman Links:**

**https://www.getpostman.com/collections/80ad03d7e8dbd880d946**

**Video Link:**

[***https://drive.google.com/file/d/1plVF39fbNoHt7r3hGrylbRXNHkvKIqxs/view***](https://drive.google.com/file/d/1plVF39fbNoHt7r3hGrylbRXNHkvKIqxs/view)

[***https://drive.google.com/file/d/1joBKEq2TxQTmjHGRaC7zRHNeyXSMYa98/view***](https://drive.google.com/file/d/1joBKEq2TxQTmjHGRaC7zRHNeyXSMYa98/view)

**Screenshots:**

[***https://i.imgur.com/sBFKWEu.png***](https://i.imgur.com/sBFKWEu.png)

[***https://i.imgur.com/G6yrezW.png***](https://i.imgur.com/G6yrezW.png)

[***https://i.imgur.com/WnZ1tGr.png***](https://i.imgur.com/WnZ1tGr.png)

[***https://i.imgur.com/eUSyBa9.png***](https://i.imgur.com/eUSyBa9.png)

![](media/image5.png){width="6.5in" height="3.6527777777777777in"}

![](media/image4.png){width="6.5in" height="3.6527777777777777in"}

![](media/image6.png){width="6.5in" height="3.6527777777777777in"}

**Reference Document:**

[***http://camel.apache.org/components.html***](http://camel.apache.org/components.html)

**Below are the dependencies added in camel docker image, so please
check the respective component in website
(http://camel.apache.org/components.html)**

1.  **Org.apache.camel (Package)**

> **Artifacts**

1.  **Camel-pdf**

2.  **Camel-aws**

3.  **Camel-bean-validator**

4.  **Camel-jdbc**

5.  **Camel-ahc**

6.  **Camel-ahc-ws**

7.  **Camel-amqp**

8.  **Camel-amqp-starter**

9.  **Camel-apns**

10. **Camel-atmosphere-websocket**

11. **Camel-atom**

12. **Camel-beanstalk**

13. **Camel-bean-validator**

14. **Camel-box**

15. **Camel-braintree**

16. **Camel-cache**

17. **Camel-cassandraql**

18. **Camel-chronicle**

19. **Camel-chunk**

20. **Camel-cmis**

21. **Camel-cometd**

22. **Camel-consul**

23. **Camel-context**

24. **Camel-couchdb**

25. **Camel-crypto**

26. **Camel-cxf**

27. **Camel-dns**

28. **Camel-disruptor**

29. **Camel-docker**

30. **Camel-dozer**

31. **Camel-ejb**

32. **Camel-ehcache**

33. **Camel-elasticsearch**

34. **Camel-etcd**

35. **Camel-spring**

36. **Camel-eventadmin**

37. **Camel-exec**

38. **Camel-facebook**

39. **Camel-flatpack**

40. **Camel-flink**

41. **Camel-fop**

42. **Camel-freemarker**

43. **Camel-ftp**

44. **Camel-ganglia**

45. **Camel-git**

46. **Camel-github**

47. **Camel-google-calendar**

48. **Camel-google-drive**

49. **Camel-google-mail**

50. **Camel-grape**

51. **Camel-geocoder**

52. **Camel-guava-eventbus**

53. **Camel-hazelcast**

54. **Camel-hipchat**

55. **Camel-hl7**

56. **Camel-http**

57. **Camel-http4**

58. **Camel-ibatis**

59. **Camel-ignite**

60. **Camel-mail**

61. **Camel-irc**

62. **Camel-ironmq**

63. **Camel-jbpm**

64. **Camel-jcache**

65. **Camel-jclouds**

66. **Camel-jcr**

67. **Camel-jgroups**

68. **Camel-jira**

69. **Camel-jms**

70. **Camel-jmx**

71. **Camel-jpa**

72. **Camel-jsch**

73. **Camel-jt400**

74. **Camel-kestrel**

75. **Camel-krati**

76. **Camel-kubernetes**

77. **Camel-kura**

78. **Camel-ldap**

79. **Camel-linkedin**

80. **Camel-lucene**

81. **Camel-lumberjack**

82. **Camel-metrics**

83. **Camel-mina**

84. **Camel-mina2**

85. **Camel-mllp**

86. **Camel-mongodb**

87. **Camel-mongodb-gridfs**

88. **Camel-mqtt**

89. **Camel-msv**

90. **Camel-mustache**

91. **Camel-mvel**

92. **Camel-nagios**

93. **Camel-nats**

94. **Camel-olingo2**

95. **Camel-openshift**

96. **Camel-optaplanner**

97. **Camel-paho**

98. **Camel-paxlogging**

99. **Camel-pgevent**

100. **camel-mail **

101. **camel-printer **

102. **camel-quartz **

103. **camel-quartz2 **

104. **camel-quickfix **

105. **camel-rabbitmq **

106. **camel-restlet **

107. **camel-rest-swagger **

108. **camel-rmi **

109. **camel-jing **

110. **camel-routebox **

111. **camel-rss **

112. **camel-salesforce **

113. **camel-sap-netweaver **

114. **camel-schematron **

115. **camel-servicenow **

116. **camel-sip **

117. **camel-sjms **

118. **camel-slack **

119. **camel-smpp **

120. **camel-snmp **

121. **camel-solr **

122. **camel-splunk **

123. **camel-spring-batch **

124. **camel-spring-integration **

125. **camel-spring-ldap **

126. **camel-spring-redis **

127. **camel-spring-ws **

128. **camel-sql **

129. **camel-ssh **

130. **camel-stax **

131. **camel-stream **

132. **camel-stomp **

133. **camel-stringtemplate **

134. **camel-telegram **

135. **camel-twilio **

136. **camel-twitter **

137. **camel-velocity **

138. **camel-vertx **

139. **camel-weather **

140. **camel-websocket **

141. **camel-xmlsecurity **

142. **camel-xmpp **

**THANK YOU**
