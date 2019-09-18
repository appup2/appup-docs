#### **Modal **

To trigger a modal handler

&lt;button @click.prevent="\_trigger('modal\_demo\_page', 'exec',
'testmodal', {'shared': {'name': 'hello', 'message': 'temp'}})"&gt; Open
Modal &lt;/button&gt;

In modal body, use blocks

&lt;block-sample-form :shared=”{{shared}}”/&gt;

In block you need to define prop shared

In template

&lt;div class=”json-display-block”&gt;{{shared}}&lt;/div&gt;

In JS

{

> props: {
>
> shared: {
>
> type: String
>
> }
>
> }

}

**Reference Link** :
[*https://bootstrap-vue.js.org/docs/components/modal/*](https://bootstrap-vue.js.org/docs/components/modal/)

#### ***Props:***

  **Property**            **Type**          **Default Value**
  ----------------------- ----------------- -------------------
  id                      String            
  title                   String            
  title-tag               String            h5
  size                    String            md
  centered                Boolean           false
  button-size             String            
  no-fade                 Boolean           false
  no-close-on-backdrop    Boolean           false
  no-close-on-esc         Boolean           false
  no-enforce-focus        Boolean           false
  header-bg-variant       String            
  header-border-variant   String            
  header-text-variant     String            
  header-class            String or Array   
  body-bg-variant         String            
  body-text-variant       String            
  modal-class             String or Array   
  body-class              String or Array   
  footer-bg-variant       String            
  footer-border-variant   String            
  footer-text-variant     String            
  footer-class            String or Array   
  hide-header             Boolean           false
  hide-footer             Boolean           false
  hide-header-close       Boolean           false
  hide-backdrop           Boolean           false
  ok-only                 Boolean           false
  ok-disabled             Boolean           false
  cancel-disabled         Boolean           false
  visible                 Boolean           false
  return-focus            Object            
  header-close-label      String            Close
  cancel-title            String            Cancel
  ok-title                String            OK
  cancel-variant          String            secondary
  ok-variant              String            primary
  lazy                    Boolean           false
  busy                    Boolean           false

#### ***Slots:***

  **Slot**             **Description**
  -------------------- --------------------------------------------------------------------------------------------------
  modal-header         Entire modal header container contents. Also removes the top right X close button.
  modal-title          Modal title. If modal-header slot is used, this slot will not be shown.
  modal-header-close   Content of Modal header close button. If modal-header slot is used, this slot will not be shown.
  modal-footer         Modal footer content. Also removes default OK and CANCEL buttons.
  modal-ok             Modal OK button content.
  modal-cancel         Modal CANCEL button content.

#### ***Events:***

  **Event**   **Arguments**                                                      **Description**
  ----------- ------------------------------------------------------------------ ------------------------------------------------------------------------------
  change      is\_visible true if modal is visible, false otherwise              new modal visibility state
  show        bvEvt BvEvent object. Call bvEvt.preventDefault() to cancel show   always emits just before modal is shown. cancelable
  shown       bvEvt BvEvent object                                               always emits when modal is shown
  hide        bvEvt BvEvent object. Call bvEvt.preventDefault() to cancel hide   always emits just before modal has hidden
  hidden      bvEvt BvEvent object                                               always emits after modal is hidden
  ok          bvEvt BvEvent object. Call bvEvt.preventDefault() to cancel hide   when default OK button pressed, just before modal has hidden. Cancelable
  cancel      bvEvt BvEvent object. Call bvEvt.preventDefault() to cancel hide   when default CANCEL button pressed, just before modal has hidden. Cancelable


