**LinkedIn - Marketplace App**

**Functionality:** In the LinkedIn app, it will generate an
authentication token to access all the apps which are provided by
LinkedIn.

**Technical Details:**

W1 (LinkedIn): In this workflow, we will use OAuth step and we provide
redirect URL for an access token, and also will pass parameters as
access\_type as offline and prompt as consent.

W2 (linkedingetaccesstoken): In this workflow will use OAuth Token and
send step.It should generate an access token for LinkedIn. The plugin
used is linked plugin.

W3 (linkedingetemail): This workflow should get the LinkedIn email id
with API LinkedIn URL.

We have to install the LinkedIn plugin with key and a secret key which
are generating while creating LinkedIn Developer account.

**Workflow Execution:**

1.we have to provide a redirect URL as a publish URL with
linkedingetaccesstoken trigger expression in workflow 1. After running
this URL in browser it will redirect to LinkedIn login page and then
generates JSON format data including accessToken.

Similarly, we have to change redirect URL as linkedingetemail with
trigger expression. I will provide linked in account mail id.

**Video:**

[*https://drive.google.com/file/d/1jPrgscUiMhOnsP9rJapmed3lFNuku6N5/view*](https://drive.google.com/file/d/1jPrgscUiMhOnsP9rJapmed3lFNuku6N5/view)

**Login Details:**

**Domain:** our.appup.com

**Username:**
[*marketplaceapps@yopmail.com*](mailto:marketplaceapps@yopmail.com)

**Password:** 123456

**Cloud:** marketplaceapps
