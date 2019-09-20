**How to setup Local publish for your app**

Step-1: Open Terminal/Command line

Step-2: execute this command &quot; **sudo su**&quot;

Step-3: &quot; **vi /etc/hosts/&quot;**

Step-4: add new line as follows,

127.0.0.1            \&lt;cloudname\&gt;.500apps.com

In case your cloud name is localapps then it should be &quot;localapps.500apps.com&quot;

Now it&#39;s time to install docker-compose and jq, this is one time installation so execute only once.

Step-5: **apt-get update                                                                  For mac**

Step-6: **apt-get install docker-compose                             brew install docker-compose**

Step-7: **apt-get install jq                                                      brew install jq**

**One time execution is completed.**

Step-8: execute the following command by entering you CLOUD\_ID and TOKEN\_URL

**curl https://s3-us-west-2.amazonaws.com/appup-libs/local-deploy/runCloud.sh | bash -s -- -c \&lt;CLOUD\_ID\&gt; -p 8080 -x 8081 -t \&lt;TOKEN\_URL\&gt;**

**Where cloud id is the cloud id (Which is typically a number) and token is JWT token that you find in your browser as cookie with name &#39;token&#39;.**

**You can find cookies in Application -\&gt; Cookies that you find in developer tools.**



(First time there will be too many downloads and they are all one time and it may take arounf 15 to 30 minutes depending upon your internet bandwidth and system performance.)

Step-9: Once the cloud is deployed on your local machine the goto browser, Enter

localhost/app-name/workflow\_trigger\_expression or

**http://** \&lt;cloudname\&gt;.500apps.com

Ensure that it is http and not https

Note: Whenever you made any changes in the workflows, just save the workflow in our.appup.com, go to appup directory and use the following command by inserting your **CLOUD\_ID , APP\_ID** and **JWT\_TOKEN**

./refresh.sh -c **\&lt;CLOUD\_ID\&gt;** -a **\&lt;APP\_ID\&gt;** -t **\&lt;JWT\_TOKEN\&gt;**



**For more detailed information regarding the setup, please click on below video**

https://drive.google.com/file/d/1K-7MHMI8D4xwzZuX8boTzLNOrYI0SwJG/view
