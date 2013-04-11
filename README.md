jQuery-Snippets
===============

A collection of jQuery Snippets


--------------------------------------------------------------------------------
###Display input text values in realtime [Demo](http://htmlpreview.github.io/?https://raw.github.com/Aproducktion/jQuery-Snippets/master/display-text-live.html)

#####Use this function
```javascript
$('#name').keyup(function () {
  $('#display').text($(this).val());
});
```

#####And this HTML:
```html
<input type="text" id="name" />
<span id="display"></span>
```

#####[Download Example](https://github.com/Aproducktion/jQuery-Snippets/blob/master/display-text-live.html)

--------------------------------------------------------------------------------
