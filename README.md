# Most-important-tuts (package manager)


composer (php)
------------------------
```
  -vendor
  -composer.json
```


npm (Node.js,JavaScrip)
------------------------
```
  -node_modules
  -package.json
```
# ----------------------

# jQuery cookie

```
<script src="https://cdnjs.cloudflare.com/ajax/libs/js-cookie/2.1.2/js.cookie.js">

  $(document).ready(function(){
  if(!Cookies.get('hide-div')){
    setTimeout(function() {
      $('#myModal').modal();
    }, 15000);
  }

  $("#sub-button").click(function () {
      Cookies.set('hide-div', true, { expires: 365 });
  });
});
This way, the modal won't open if the client already has the 'hide-div' cookie set to true.
```

  
