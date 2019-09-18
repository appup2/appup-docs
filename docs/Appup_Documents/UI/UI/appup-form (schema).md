### Form-JSON

**name**: that you want to see in deserialized,

**label** : To display

**description**: to display down the field,

**type**:to give the type of field text/button/dropdown etc.

**class**: that you want to bind to that field.

**id**: is like normal html id which should be unique.

**url**: to display the route params that you want to show in your url &
you can also get json data as an input to be displayed in page.

**computational** : will update the present url with the url that your
provided in url field

**options**: that have to be displayed in the dropdown box

**required** : is like a condition which checks for true value and
evaluate the given input.

**key\_label :** that to be displayed

**key\_value:** like a value here to store value of the option.

**buttons** : is an array you can pass object in side that like
label,function,type,variant

new properties added:

**checked** : if set to true, the checked options of checkboxes, radios
and select fields will get selected.

### QuillJS:

"fields": \[{

"name": "name",

"label": "Name",

"description": "Please enter your name",

"placeholder": "Enter your name",

"id": "first\_name",

"type": "quilljs",

"required": true,

"class": "col-sm-12 col-md-6"

}\]

(or)\
\
We can use directly quilljs as below format\
\
&lt;appup-quilljs :config = {"debug": "info","placeholder": "Compose an
epic...", "readOnly": true,"theme": "snow"}
:s3presignurl=”appuppresignurl” :id=”id” &gt;

### Checkboxes

"fields": \[{

"id": “radio1”,

"type": "checkbox",

"name": "checkbox",

"label": "Checkbox",

"option": \[

{

"label": "Pineapple",

"value": "pineapple"

},

{

"label": "Grape",

"value": "grape",

"disabled": true

}

\],

"required": true

}\]

### Radio    

"fields": \[{

"id": 50,

"type": "radio",

"name": "radio",

"label": "Radio",

"option": \[

{

"label": "Male",

"value": "Male"

},

{

"label": "Female",

"value": "Female",

"disabled": true

}

\],

"required": true

}\]

### Select

“fields”:\[{

"id": 10,

"type": "dropdown",

"name": "cloud\_type",

"label": "Cloud Type",

"option": \[{

"value": null,

"label": "Please select an option"

},

{

"value": "Appup",

"label": "Appup"

},

{

"value": "Amazon",

"label": "Amazon"

},

{

"value": "Google",

"label": "Google"

}

\],

"required": true,

"class": "col-sm-12 col-md-6 select"

}\]

### Multiselect

“fields”:\[{

id: "70",

**type**: "multiselect",

name: "multiselect",

label: "Multiselect",

option: \[

{

value: **null**,

label: "Please select an option"

},

{

value: "js",

label: "Javascript"

},

{

value: "java",

label: "Java"

},

{

value: "ruby",

label: "Ruby"

},

{

value: "php",

label: "PHP",

disabled: **true**

}

\],

required: **true**

}\]

### &lt;appup-datetime type="date" placeholder="Choose Date here" v-model="date" &gt;&lt;/appup-datetime&gt;Datetime

fields: \[

{

type: "appup-datetime",

name: "date",

input: "date",

label: "Date Picker",

placeholder: "Date here"

},

{

type: "appup-datetime",

name: "time",

input: "time",

label: "Time Picker",

placeholder: "Time here"

},

{

type: "appup-datetime",

name: "date\_time",

input: "datetime",

label: "Datetime Picker",

placeholder: "DateTime here"

},

{

type: "appup-datetime",

name: "date\_range",

input: "daterange",

label: "Datetime Picker",

placeholder: "DateTime here"

}

\]

}

**Form JSON Format:**{
----------------------

"contacts": {

"fields": \[{

"name": "name",

"label": "Name",

"description": "Please enter your name",

"placeholder": "Enter your name",

"id": "first\_name",

"type": " ",

"required": true,

"class": "col-sm-12 col-md-6"

}, {

"id": 10546,

"type": "text",

"name": "URL",

"label": "URL",

"required": true,

"class": "col-sm-12 col-md-6"

},

{

"id": 1090,

"type": "text",

"label": "Friendly URL",

"name": "url2",

"required": true,

"computation":
"'https://'+form.URL.replace(/\[\^a-z0-9\]/gi,'').toLowerCase()+'.appup.cloud'",

"disabled": true,

"class": "col-sm-12 col-md-6"

},

{

"id": 10,

"type": "dropdown",

"name": "cloud\_type",

"label": "Cloud Type",

"option": \[{

"value": null,

"label": "Please select an option"

},

{

"value": "Appup",

"label": "Appup"

},

{

"value": "Amazon",

"label": "Amazon"

},

{

"value": "Google",

"label": "Google"

}

\],

"required": true,

"class": "col-sm-12 col-md-6 select"

},

{

"id": 106573,

"type": "text",

"name": "SERVER\_URL",

"label": "Enter Server URL",

"required": true,

"condition": "form.cloud\_type!=null && this.form.cloud\_type=='Appup'",

"class": "col-sm-12 col-md-6 red"

},

{

"id": 10,

"type": "dropdown",

"name": "name",

"label": "Select Name",

"key\_value": "id",

"key\_label": "name",

"url": "https://jsonplaceholder.typicode.com/users/",

"required": true,

"class": "col-sm-12 col-md-6 select"

},

{

"id": 50,

"type": "checkbox",

"name": "checkbox",

"label": "Checkbox",

"option": \[

{

"label": "Pineapple",

"value": "pineapple"

},

{

"label": "Grape",

"value": "grape",

"disabled": true

}

\],

"required": true

}

\],

"buttons": \[{

"label": "Submit",

"variant": "primary",

"type": "submit",

"function": "onSubmit"

},{

"label": "Submit",

"variant": "primary",

"type": "submit",

"function": "onSubmit"

},

{\
id: "70",\
type: "multiselect",\
name: "multiselect",\
label: "Multiselect",\
option: \[\
{\
value: null,\
label: "Please select an option"\
},\
{\
value: "js",\
label: "Javascript"\
},\
{\
value: "java",\
label: "Java"\
},\
{\
value: "ruby",\
label: "Ruby"\
},\
{\
value: "php",\
label: "PHP",\
disabled: true\
}\
\],\
required: true\
},

{

id: "70",

**type**: "multiselect",

name: "multiselect",

label: "Multiselect",

option: \[

{

value: **null**,

label: "Please select an option"

},

{

value: "js",

label: "Javascript"

},

{

value: "java",

label: "Java"

},

{

value: "ruby",

label: "Ruby"

},

{

value: "php",

label: "PHP",

disabled: **true**

}

\],

required: **true**

},

"post": "https://our.appup.com/login"

}

}

### Horizontal Form

JSON

{

"formJson": {

"fields": \[

{

"id": "r\_name",

"type": "text",

"name": "first\_name",

"placeholder": "Enter name",

"label": "Company Name",

**"class":"col-md-12",**

"required": true,

"vmessage": "First Name"

},

{

"id": "r\_age",

"type": "text",

"name": "age",

"placeholder": "Enter age",

"label": "User Name",

**"class":"col-md-3",**

"required": true,

"vmessage": "Age"

},

{

"id": "r\_number",

"type": "text",

"name": "Email Address",

"placeholder": "Enter mobile number",

"label": "Mobile number",

"class":"col-md-4",

"required": true,

"vmessage":"Mobile NUmber"

},

{

"id": "r\_name",

"type": "text",

"name": "sd",

"placeholder": "Enter name",

"label": "First Name",

"class":"col-md-6",

"required": true,

"vmessage": "First Name"

},

{

"id": "r\_age",

"type": "text",

"name": "dasd",

"placeholder": "Enter age",

"label": "Last Name",

"class":"col-md-6",

"required": true,

"vmessage": "Age"

},

{

"id": "r\_number",

"type": "text",

"name": "sadasdwew",

"placeholder": "Enter mobile number",

"label": "Address",

"class":"col-md-12",

"required": true,

"vmessage":"Mobile NUmber"

},

{

"id": "r\_name",

"type": "text",

"name": "yujnr",

"placeholder": "Enter name",

"label": "City",

"class":"col-md-4",

"required": true,

"vmessage": "First Name"

},

{

"id": "r\_age",

"type": "text",

"name": "artgge",

"placeholder": "Enter age",

"label": "Postal Code",

"class":"col-md-3",

"required": true,

"vmessage": "Age"

},

{

"id": "r\_number",

"type": "text",

"name": "yujynfd",

"placeholder": "Enter mobile number",

"label": "Country",

"class":"col-md-5",

"required": true,

"vmessage":"Mobile NUmber"

},

{

"id": "r\_name",

"type": "textarea",

"name": "iuerhljknl",

"placeholder": "Enter name",

"label": "About Me",

"class":"col-md-12",

"required": true,

"vmessage": "First Name"

}

\],

"buttons": \[

{

"label": "Sign up",

"variant": "btn btn-primary",

"type": "submit",

"class":"testing"

},

{

"label": "Reset",

"variant": "btn btn-danger",

"type": "submit",

"class":"testing"

}

\],

"urls": {

"post": "/register",

"next": "/login"

},

"messages": {

"error": "Email already exists."

},

"buttonAt":"top"

}

}

In template

&lt;div&gt;

&lt;appup-form preload="pre\_load" submit="submit"

:workflow\_params='{entity:"formJson"}'

&gt;&lt;/appup-form&gt;

&lt;/div&gt;
