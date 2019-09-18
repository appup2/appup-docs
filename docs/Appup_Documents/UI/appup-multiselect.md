***&lt;appup-multiselect&gt;***

---&gt; appup-multiselect is dropdown component in which dropdown list
will be generated in both static(By sending data throw **options** prob
) and dynamically ( by sending link Url throw **url** prob )

### **Features & characteristics:**

-   Dropdowns

-   Filtering(search)

-   V-model support

-   Single select

-   Multiple select

**&lt;How to use&gt;**

**--&gt;&lt;sample-code&gt;**

  -----------------------------------------------------------------------
  &lt;template&gt;\
  &lt;div&gt;\
  &lt;h6&gt;Multiselect with manual options&lt;/h6&gt;\
  &lt;appup-multiselect\
  :id="item.id"\
  :options="item.option"\
  v-model="itemValue"\
  @input="onInput"\
  :state="false"\
  :url="item.url ? item.url : null"\
  :key\_value="item.key\_value ? item.key\_value : null"\
  :key\_label="item.key\_label ? item.key\_label : null"\
  /&gt;\
  \
  &lt;h6&gt;Multiselect with options fetched from URL&lt;/h6&gt;\
  \
  &lt;appup-multiselect\
  :id="dynamicItem.id"\
  :options="dynamicItem.option"\
  v-model="dynamicItemValue"\
  @input="onInput"\
  :state="false"\
  :url="dynamicItem.url ? dynamicItem.url : null"\
  :key\_value="dynamicItem.key\_value ? dynamicItem.key\_value : null"\
  :key\_label="dynamicItem.key\_label ? dynamicItem.key\_label : null"\
  /&gt;\
  \
  &lt;h6&gt;Tags&lt;/h6&gt;\
  \
  &lt;/template&gt;\
  \
  &lt;script&gt;\
  export default {\
  data() {\
  return {\
  item: {\
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
  },\
  itemValue: "",\
  dynamicItem: {\
  id: "80",\
  type: "multiselect",\
  name: "multiselectDynamic",\
  label: "Multiselect with Options from url",\
  url: "http://www.mocky.io/v2/5b507e3a3600003b14dd0e66",\
  key\_value: "value",\
  key\_label: "label",\
  required: true\
  },\
  dynamicItemValue: ""\
  };\
  },\
  methods: {\
  onInput(e) {\
  console.log(this.item);\
  }\
  }\
  };\
  &lt;/script&gt;
  -----------------------------------------------------------------------

**&lt;probs&gt;**

  > **id**            Integer||String                                      Used to identify the component in events.
  ------------------- ---------------------------------- ----------------- ----------------------------------------------------------------------------------------------------------------------------
  > **options**       > Array                                              Array of available options: Objects, Strings or Integers. If array of objects, visible label will default to option.label.
  > **value**         > Object||Array||String||Integer                     Presets the selected options.
  > **url**           > text                                               Dynamic dropdown list
                                                                           
  > **label**         > String                                             Label from option Object, that will be visible in the dropdown.
  > **searchable**    > Boolean                          true              Add / removes search input.
                                                                           
                                                                           
  > **placeholder**   > String                           'Select option'   Equivalent to the placeholder attribute on a &lt;select&gt; input.


