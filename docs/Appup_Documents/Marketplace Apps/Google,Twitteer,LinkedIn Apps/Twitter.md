**Twitter - Marketplace App**

**Functionality:** In the Twitter app, it will generate an
authentication token to access all the apps which are provided by
Twitter.

**Technical Details: **

W1 (Twitter): In this workflow, we will use OAuth step and we provide
redirect URL for an access token, and also will pass parameters as
access\_type as offline and prompt as consent.

W2 (twitterhandler): In this workflow will use OAuth Token and send
step.It

should generate an access token for a Twitter account. The plugin used
is a Twitter plugin.

We have to install the LinkedIn plugin with key and a secret key which
are generating while creating a Twitter Developer account.

**Workflow Execution:**

1.we have to provide a redirect URL as a publish URL with twitter
handler workflow trigger expression in workflow 1. After running this
URL in browser it will redirect to a Twitter login page and then
generates JSON format data including accessToken.

**Video:**
https://drive.google.com/file/d/1jPrgscUiMhOnsP9rJapmed3lFNuku6N5/view

**Login Details:**

**Domain:** our.appup.com

**Username:**
[*marketplaceapps@yopmail.com*](mailto:marketplaceapps@yopmail.com)

**Password:** 123456

**Cloud:** marketplaceapps
