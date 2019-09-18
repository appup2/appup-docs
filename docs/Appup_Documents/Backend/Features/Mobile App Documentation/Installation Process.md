**Commands to install 500apps mobile app:**

a)wget
[*https://appup-apk.s3-us-west-1.amazonaws.com/script.sh*](https://appup-apk.s3-us-west-1.amazonaws.com/script.sh)

Run this command to download script file.

b)sh script.sh

To run the downloaded script file.

1\) app\_parent\_dir ----&gt; preferred location of your app"

Location to be specified for parent directory where app has to be
placed.

2\) app\_name ----&gt; specify your app name"

Specify the app name. For example, if we give “trackly”, it creates with
app name “trackly”.

3)docker run -v \$app\_parent\_dir:/data webratio/cordova cordova create
\$app\_name

This command actually runs the cordova and places the files in the
directory created.

4)echo "\$app\_dir ----&gt; Give app\_parent\_dir/app\_name"

Mention the complete path. (location of your app)

5)echo "\$cloud\_id

Mention the cloud id.

6)echo "\$cloud\_name

Mention your cloud name.
