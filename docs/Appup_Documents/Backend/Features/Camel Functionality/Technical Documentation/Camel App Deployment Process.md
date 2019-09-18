
**Camel App Deployment Process:**

Camel app contains one workflow with two steps, one is camel generic
step and one is send step . Camel generic step will take the uri and it
will process , send step will give the output of the camel step.

Camel app we have to publish in the camel docker image because jars
conflicts with the aws steps , To deploy camel app we have to follow
below steps.

1.  We have camel generic step in appup-camel-repo , we have to add
    > “appup-camel-repo” in docker-clean-build.sh is for clean and build
    > docker for “appup-camel-repo” and mvn.sh is to run pom.xml , for
    > copying dependencies to app-lib and prepare jar.

2.  We have to remove conflicting aws dependencies from step-externals.

3.  We have to run temp.sh with sudo command.

4.  We need to provide new docker image to create docker image for
    > camel.

5.  We have provide Y / N to push docker image to
    > “applet/applet-io-dev”.

After restarting , docker image will push to qa

Once docker image is pushed we will see which we created docker image
tag in the docker image tag list publish screen. Like below.

//image insert

After docker image is pushed to QA, we can use camel step to create a
camel app and need to publish in the camel docker.

We can use our camel app for different components with passing uri ,
headersand message from postman hitting camel app.
