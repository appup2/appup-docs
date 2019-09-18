**Automation ( Task Sequence Step ) - Marketplace App**

**Functionality:**

Task sequence app executes multiple tasks in sequence mode. All the REST
API calls are provided and all the tasks related to payload data is
provided in the JSON format.So based on the sequence we provide all the
rest API calls gets executed.

**Technical Details:**

W1(REST\_EMAIL):\
This workflow should send a message to respective mail-id.\
\
W2(SELECT\_DATA):\
This workflow should get data from DB.\
\
W3(EMAIL\_CONTENT):\
This workflow should get the email content to sent from DB.\
\
W4(TASKSEQUENCE\_WORKFLOW)\
This workflow should execute the remaining workflows in a sequence based
on tasks type and URL.

**PostMan Collections:**

[***https://www.getpostman.com/collections/d1b82bc07d478502c75b***](https://www.getpostman.com/collections/d1b82bc07d478502c75b)

**Videos:**

[***https://drive.google.com/file/d/1kyKtTqo0C\_vnQjsD9DGtoEkMB91oE\_ht/view***](https://drive.google.com/file/d/1kyKtTqo0C_vnQjsD9DGtoEkMB91oE_ht/view)

**Login Details:**

**Domain:** our.appup.com

**Username:**
[*marketplaceapps@yopmail.com*](mailto:marketplaceapps@yopmail.com)

**Password:** 123456

**Cloud:** marketplaceapps
