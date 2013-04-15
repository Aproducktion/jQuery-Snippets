jQuery-Snippets
===============

A collection of jQuery Snippets


--------------------------------------------------------------------------------
###Display input  values in realtime 

#####Use this function for Text
```javascript
$('#name').keyup(function () {
  $('#display-text').text($(this).val());
});
```

#####Use this function for Options Selects
```javascript
$('#name').bind("change keyup", function(event){
  $('#display-select').text($(this).val());
});
```



#####And this HTML:
```html
<input type="text" id="name" />
<span id="display-text"></span>
<br>
<select id="name">
  <option value="volvo">Volvo</option>
</select>
<span id="display-select"></span>
```

#####[Download Example](https://github.com/Aproducktion/jQuery-Snippets/blob/master/display-text-live.html) | [Live Demo](http://htmlpreview.github.io/?https://raw.github.com/Aproducktion/jQuery-Snippets/master/display-text-live.html)

--------------------------------------------------------------------------------
