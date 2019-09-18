Slideout Component
------------------

Use slideout component to show a page as a slideout in another page.

**Slideout parent page:** The page which invokes a slideout page

**Slideout page:** The page which is referenced from slideout parent
page

### Usage

Add slideout component in a page where you want to show a slideout.

**In slideout parent page:**

&lt;appup-slideout route="**/view/:id**"&gt;&lt;/appup-slideout&gt;

Provide a page route as a value to route prop.

How to invoke a slideout page?

Suppose route of this page is **/people** and route of slideout page is
**/view/:id**

Then slideout url become **/people/view/:id** (parent route + child
route)

Eg: /people/view/123

Note: self closing tag for appup-slideout component will not work eg:
&lt;appup-slideout route="/view/:id"/&gt;

Demo:
[*https://ui.appup.cloud/demos/\#/people*](https://ui.appup.cloud/demos/#/people)

### Props

route ***String*** (*required*)

Appup runtime uses route to find a page and set child route

eg: /view/:id

align ***String*** (*optional*) default: 'right'

Determines alignment of slideout panel

accepted values: left, right

close-btn ***String*** (*optional*) default: 'show'

If value is "show", close button is shown - when clicked closes the
panel

To add custom close button, set prop to "hide"

eg:

&lt;appup-slideout route="/edit/:id"
close-btn="hide"&gt;&lt;/appup-slideout&gt;\
In slideout page: create a custom button as follows\
&lt;button v-on:click="\$parent.close()"&gt;Close Slideout
Panel&lt;/button&gt;

### Methods

close()

Closes slideout panel

Useful when creating custom close button in slideout page

eg:

&lt;button v-on:click="\$parent.close()"&gt;Close Slideout
Panel&lt;/button&gt;

### Sample

In Slideout parent page

route: /people

&lt;div class="py-5"&gt;

&lt;div class="container"&gt;

&lt;div class="row"&gt;

&lt;div class="col-md-4"&gt;

&lt;div class="card"&gt;

&lt;div class="card-block"&gt;

&lt;h4 class="card-title"&gt;Card title&lt;/h4&gt;

&lt;h6 class="card-subtitle text-muted"&gt;Support card
subtitle&lt;/h6&gt;

&lt;p class="card-text p-y-1"&gt;Some quick example text to build on the
card title .&lt;/p&gt;

**&lt;a href="\#/people/view/1" class="card-link"&gt;link&lt;/a&gt;**

&lt;a href="\#" class="card-link"&gt;Second link&lt;/a&gt;

&lt;/div&gt;

&lt;/div&gt;

&lt;/div&gt;

&lt;div class="col-md-4"&gt;

&lt;div class="card"&gt;

&lt;div class="card-block"&gt;

&lt;h4 class="card-title"&gt;Card title&lt;/h4&gt;

&lt;h6 class="card-subtitle text-muted"&gt;Support card
subtitle&lt;/h6&gt;

&lt;p class="card-text p-y-1"&gt;Some quick example text to build on the
card title .&lt;/p&gt;

&lt;a href="\#/people/view/2" class="card-link"&gt;link&lt;/a&gt;

&lt;a href="\#" class="card-link"&gt;Second link&lt;/a&gt;

&lt;/div&gt;

&lt;/div&gt;

&lt;/div&gt;

&lt;div class="col-md-4"&gt;

&lt;div class="card"&gt;

&lt;div class="card-block"&gt;

&lt;h4 class="card-title"&gt;Card title&lt;/h4&gt;

&lt;h6 class="card-subtitle text-muted"&gt;Support card
subtitle&lt;/h6&gt;

&lt;p class="card-text p-y-1"&gt;Some quick example text to build on the
card title .&lt;/p&gt;

&lt;a href="\#/people/view/3" class="card-link"&gt;link&lt;/a&gt;

&lt;a href="\#" class="card-link"&gt;Second link&lt;/a&gt;

&lt;/div&gt;

&lt;/div&gt;

&lt;/div&gt;

&lt;/div&gt;

&lt;/div&gt;

**&lt;appup-slideout align="right" class="my-class"
route="/view/:id"&gt;&lt;/appup-slideout&gt;**

&lt;/div&gt;

In slideout page

**route: /view/:id**

&lt;div&gt;

&lt;h3&gt;Dummy body {{\$route.params.id}}&lt;/h3&gt;

&lt;/div&gt;
