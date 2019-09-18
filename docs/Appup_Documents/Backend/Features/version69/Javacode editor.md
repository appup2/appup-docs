**Functionality:**

Java code editor is used to compile your java program. For this a code
editor is provided where the java program has to be placed and based on
the dependency provided, it gets compiled and result is shown.

**Prerequisites:**

1)Install ‘Java plugin’. For this provide POM data that is required for
your java program.

2)Inside the java code editor select the required ‘Maven Dependency
Plugin’.

For example, my java program is about to send an email and for this the
following dependency is added.

&lt;dependencies&gt;

&lt;dependency&gt;

&lt;groupId&gt;com.appup&lt;/groupId&gt;

&lt;artifactId&gt;steps-api&lt;/artifactId&gt;

&lt;scope&gt;system&lt;/scope&gt;

&lt;version&gt;1.0.1&lt;/version&gt;

&lt;systemPath&gt;/appup\_lib/jars/appup\_jars/steps-api-1.0.1.jar&lt;/systemPath&gt;

&lt;/dependency&gt;

&lt;/dependencies&gt;

&lt;repositories&gt;

&lt;repository&gt;

&lt;id&gt;central&lt;/id&gt;

&lt;name&gt;Maven Repository Switchboard&lt;/name&gt;

&lt;layout&gt;default&lt;/layout&gt;

&lt;url&gt;http://repo1.maven.org/maven2&lt;/url&gt;

&lt;snapshots&gt;

&lt;enabled&gt;false&lt;/enabled&gt;

&lt;/snapshots&gt;

&lt;/repository&gt;

&lt;/repositories&gt;

3)In the java program include the package name as well.

4)And the java class name should be mentioned as name for java code
editor ‘Name’.

5)Workflows-&gt;Developers ’Java code executor’ is the workflow node
which is used to execute the code editor class.

Please check the screenshots attached below:

![](media/image10.png){width="6.5in" height="3.6527777777777777in"}

![](media/image1.png){width="6.5in" height="3.6527777777777777in"}

![](media/image2.png){width="6.5in" height="3.6527777777777777in"}

![](media/image3.png){width="6.5in" height="3.6527777777777777in"}

![](media/image7.png){width="6.5in" height="3.6527777777777777in"}

![](media/image5.png){width="6.5in" height="3.6527777777777777in"}

![](media/image4.png){width="6.5in" height="3.6527777777777777in"}

![](media/image9.png){width="6.5in" height="3.6527777777777777in"}

![](media/image8.png){width="6.5in" height="3.6527777777777777in"}

![](media/image6.png){width="6.5in" height="3.6527777777777777in"}
