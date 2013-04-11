jQuery-Snippets
===============

A collection of jQuery Snippets


--------------------------------------------------------------------------------
###Display input text values in realtime

####Use this function
```javascript
$('#name').keyup(function () {
  $('#display').text($(this).val());
});
```

####And this HTML:
```html
<input type="text" id="name" />
<span id="display"></span>
```
--------------------------------------------------------------------------------
