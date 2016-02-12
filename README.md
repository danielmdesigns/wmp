# What's My Parameter?
Pass a paramater in a url from one page to another.

Need to read, find and get parameter value(s) from a URL string of a current page and/or email newsletter to be able to perform some type of action? We'll here ya go...

**INSTALL**

1: Install jQuery onto the page(s) where you need to provide an action.

```
<script src="https://code.jquery.com/jquery-2.2.0.min.js"></script>
```

2: Now copy&paste the wmParameter

```
function wmParameter(findParam){ 
  var pageURL = window.location.search.substring(1); 
  var splitURL = pageURL.split('&'); 
  for(var i = 0; i < splitURL.length; i++){ 
    var paramName = splitURL[i].split('='); 
    if(paramName[0] === findParam){ 
      return paramName[1]; 
    } 
  } 
} 

var thisParameter = wmParameter("test"); 

if (thisParameter === "abc"){ 
  alert("The parameter of '" + thisParameter + "' was passed to this page successfully!"); 
}else{ 
  alert("There is no paramter to display."); 
}
```

3: If your alert's are successful, replace with your jQuery action.

```
$("element").method("property");
```

