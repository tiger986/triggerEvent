## Events that trigger the element when clicking on an area other than the element
#### HTML code
```html
<div class="box">
    <div class="d1">Click outside</div>
</div>
  ```
####JS code
```javascript
$(function(){		
    $(document).click(function(e){
        var target = $(e.target);
	if(target.closest('.d1').length == 0){
            alert("Clicking on the outside of d1");		
	}
    });	
})
