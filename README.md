jQuery keypad plugin
====================
This plugin is made for displaying numeric keypad on touchscreen devices. Try [demo](http://rawgit.com/visionect/keypad/master/demo.html).

Usage
-----
* Include `jquery.keypad.css` in head of your html document.

  ```
  <link rel="stylesheet" type="text/css" href="jquery.keypad.css">
  ```

* Include `jquery.keypad.js` at the bottom after jQuery.

  ```
  <script type="text/javascript" src="http://code.jquery.com/jquery-1.11.0.min.js"></script>
  <script type="text/javascript" src="jquery.keypad.js"></script>
  ```

* Use `keypad` function on jQuery object.

  ```
  $(document).ready(function() {
      $('#keypad').keypad();
  });
  ```

By default it will write the value to input with class name `keypad` (you can change that with options) and will submit the form that input is in, when `ok` button is pressed.

Advance options
---------------
You can customize the plugin by providing a hash with options on initialization. eg:

```
$(document).ready(function() {
    $('#keypad').keypad({
        inputField: $('form #keypadinput'),
        submitButtonText: 'enter'
    });
});
```

Default options:

```
{
    inputField: 'input.keypad', //can be jQuery selector or jQuery object
    buttonTemplate: '<button></button>',
    submitButtonText: 'ok',
    deleteButtonText: 'del',
    submitButtonClass: 'submit',
    deleteButtonClass: 'delete'
}
```