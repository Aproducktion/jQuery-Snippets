jQuery-Snippets
===============

A collection of jQuery Snippets


--------------------------------------------------------------------------------
###Display input  values in realtime 

#####Use this function for Text Input Elements
```javascript
$('#name').keyup(function () {
  $('#display-text').text($(this).val());
});
```
#####Use this function for Select Elements
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
###REUSABLE REPEATER FIELD	FUNCTION

#####Add this script to your file
```
// REUSABLE REPEATER FIELD	FUNCTION
// ------------------------------------------------------------
var maxInputs = 20; //maximum input boxes allowed
var fieldCount = 1; //Track the field amounts

	$.fn.repeater = function() {
		this.each(function() {
		    
		    var $fieldWrapper = $(this);

		    $fieldWrapper.find(".add-field").click(function(e) {
		    	if(fieldCount <= maxInputs) //max input boxes allowed
		    	{
		        	$('.field:first-child', $fieldWrapper).clone(true).appendTo($fieldWrapper).find('input').val('').focus();
		        	fieldCount++;//text box added increment
		    	}
		    });
		    $('.field .remove-field', $fieldWrapper).click(function() {
		        if ($fieldWrapper.find('.field').length > 1)
		        {
		        	$(this).parent('.field').remove();
		        }    
		        fieldCount--
		    });
		});
	return this;
	};
// ------------------------------------------------------------

$('.repeater-field').repeater();
```
#####And this HTML:
```
<div class="repeater-field">
	<div class="field phone">
		{{ Form::label('store_phone_number', 'Phone') }}
		{{ Form::text('store_phone_number', '', array('placeholder' => '+01 (xxx) xxx-xxxx')) }}
		<button type="button" class="ui button mini green add-field">Add field</button>
		<button type="button" class="ui button mini red remove-field">Remove</button>
	</div>
</div>
```



