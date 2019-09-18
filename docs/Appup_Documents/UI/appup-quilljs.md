### **&lt;appup-quilljs&gt;**

---&gt; The &lt;textarea&gt; provides a native and essential solution to
almost any web application. But at some point you may need to add
formatting to text input. This is where rich text editors come in. There
are many solutions to choose from, but &lt;appup-quilljs&gt; brings a
few modern ideas to consider.

### ***To use with form schema***

**Default**

  --------------------------------
  {\
  "all\_form\_fields\_quill": {\
  "fields": \[\
  \
  {\
  \
  "type": "quilljs",\
  }\
  \]\
  }\
  }
  --------------------------------

**Configurable **

+-----------------------------------------------------------------------+
| {\                                                                    |
| "all\_form\_fields\_quill": {\                                        |
| "fields": \[\                                                         |
| {\                                                                    |
| \                                                                     |
| "type": "quilljs",\                                                   |
| "config": {\                                                          |
| "debug": "error",\                                                    |
| "placeholder": "i am hemanth..",\                                     |
| "readOnly": "true",\                                                  |
| "theme": "bubble",\                                                   |
| "modules": {\                                                         |
| "toolbar": \[\                                                        |
| \["link"\]                                                            |
|                                                                       |
| \['bold', 'italic', 'underline', 'strike'\],\                         |
| \['blockquote', 'code-block'\],\                                      |
| \[{ 'header': 1 }, { 'header': 2 }\],\                                |
| \[{ 'list': 'ordered'}, { 'list': 'bullet' }\],\                      |
| \[{ 'script': 'sub'}, { 'script': 'super' }\],\                       |
| \[{ 'indent': '-1'}, { 'indent': '+1' }\],\                           |
| \[{ 'direction': 'rtl' }\],                                           |
|                                                                       |
| \]\                                                                   |
| }\                                                                    |
| }\                                                                    |
| \                                                                     |
| \                                                                     |
| }\                                                                    |
| \]\                                                                   |
| }\                                                                    |
| }                                                                     |
+=======================================================================+
|                                                                       |
+-----------------------------------------------------------------------+
|                                                                       |
+-----------------------------------------------------------------------+

### ***To use outside form schema (in template)***

**Default **

  -------------------------------
  &lt;div&gt;\
  &lt;h1&gt;defualt&lt;/h1&gt;\
  &lt;appup-quilljs /&gt;\
  &lt;/div&gt;
  -------------------------------

**Configurable **

+-----------------------------------------------------------------------+
| &lt;appup-quilljs\                                                    |
| config={\                                                             |
| \                                                                     |
| debug: "error",\                                                      |
| placeholder: "i am hemanth..",\                                       |
| readOnly: true,\                                                      |
| theme: "bubble",\                                                     |
| \                                                                     |
| modules: {\                                                           |
| toolbar: \[\                                                          |
| \['bold', 'italic', 'underline', 'strike'\],\                         |
| \['blockquote', 'code-block'\],\                                      |
| \[{ 'header': 1 }, { 'header': 2 }\],\                                |
| \[{ 'list': 'ordered'}, { 'list': 'bullet' }\],\                      |
| \[{ 'script': 'sub'}, { 'script': 'super' }\],\                       |
| \[{ 'indent': '-1'}, { 'indent': '+1' }\],\                           |
| \[{ 'direction': 'rtl' }\],\                                          |
| \                                                                     |
| \[{ 'size': \['small', false, 'large', 'huge'\] }\],\                 |
| \[{ 'header': \[1, 2, 3, 4, 5, 6, false\] }\],\                       |
| \                                                                     |
| \[{ 'color': \[\] }, { 'background': \["red","black"\] }\], \[{       |
| 'font': \[\] }\],\                                                    |
| \[{ 'align': \[\] }\],\                                               |
| \['image'\],\                                                         |
| \['video'\],\                                                         |
| \['link'\],\                                                          |
| \['formula'\],\                                                       |
| \                                                                     |
| \['clean'\]                                                           |
|                                                                       |
| \]\                                                                   |
| }\                                                                    |
| }\                                                                    |
| 0\                                                                    |
| \                                                                     |
| s3presignurl="https://ui.appup.cloud/examples/upload?file\_name='"\   |
| /&gt;                                                                 |
+=======================================================================+
|                                                                       |
+-----------------------------------------------------------------------+

**Props:**

**Config**

**→** To configure appup-quilljs, pass in an config object

Config object structure

  -------------------------------------
  config: {\
  debug: 'info',\
  modules: {\
  toolbar: '\#toolbar'\
  },\
  placeholder: 'Compose an epic...',\
  readOnly: true,\
  theme: 'snow'\
  };
  -------------------------------------

**Debug**

→ Default: warn

Shortcut for [*debug*](https://quilljs.com/docs/api/#debug). Note debug
is a static method and will affect other instances of Quill editors on
the page. Only warning and error messages are enabled by default.

Static method enabling logging messages at a given level: 'error',
'warn', 'log', or 'info'. Passing true is equivalent to passing 'log'.
Passing false disables all messages.

### **Modules **

→ Modules allow Quill’s behavior and functionality to be customized.

Modules object structure

  -------------------------------------
  modules: {\
  toolbar: '\#toolbar' // type array\
  },
  -------------------------------------

**Toolbar**

→ The Toolbar module allow users to easily format Quill’s contents.

![](media/image1.png){width="6.270833333333333in"
height="1.0277777777777777in"}

  ---------------------------------------------------------------------------------------------------
  toolbar: \[\
  \['bold', 'italic', 'underline', 'strike'\], // toggled buttons\
  \['blockquote', 'code-block'\],\
  \[{ 'header': 1 }, { 'header': 2 }\], // custom button values\
  \[{ 'list': 'ordered'}, { 'list': 'bullet' }\],\
  \[{ 'script': 'sub'}, { 'script': 'super' }\], // superscript/subscript\
  \[{ 'indent': '-1'}, { 'indent': '+1' }\], // outdent/indent\
  \[{ 'direction': 'rtl' }\], // text direction\
  \[{ 'size': \['small', false, 'large', 'huge'\] }\], // custom dropdown\
  \[{ 'header': \[1, 2, 3, 4, 5, 6, false\] }\],\
  \
  \[{ 'color': \[\] }, { 'background': \["red","black"\] }\], // dropdown with defaults from theme\
  \[{ 'font': \[\] }\],\
  \[{ 'align': \[\] }\],\
  \['image'\],\
  \
  \['link'\],\
  \
  \
  \
  \['clean'\] // remove formatting button\
  \]
  ---------------------------------------------------------------------------------------------------
  ---------------------------------------------------------------------------------------------------

**Placeholder **

**→** Placeholder text to show when editor is empty.

#### **ReadOnly **

Default: false

Whether to instantiate the editor to read-only mode.

#### **Theme**

Name of theme to use. The builtin options are “bubble” or “snow”. An
invalid or falsy value will load a default minimal theme. Note the
theme’s specific stylesheet still needs to be included manually.

**S3presignurl**

**→** S3presignurl is used to save image in s3 bucket

Requied :

Plugin

Workflow

Trigger

s3presignurl="https://ui.appup.cloud/examples/upload?file\_name='"

https://ui.appup.cloud → cloud url

/examples→ project name

/upload --&gt;trigger name

*Workflow*

[*https://snag.gy/BwCktH.jpg*](https://snag.gy/BwCktH.jpg)

[*https://snag.gy/ZjXLE1.jpg*](https://snag.gy/ZjXLE1.jpg)

[*https://snag.gy/Iil7rV.jpg*](https://snag.gy/Iil7rV.jpg)

*Trigger *

[*https://snag.gy/Hd98Pa.jpg*](https://snag.gy/Hd98Pa.jpg)

Sample output

[*https://ui.appup.cloud/examples/\#/appup-quilljs*](https://ui.appup.cloud/examples/#/appup-quilljs)
