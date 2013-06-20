### A Very Simple HTML Template Engine

Simple Use
-----

```HTML
    <ul>
    <%  for(var i = 0; i < year.length; i++){ %>
        <li>Happy <%year[i]%> Year!</li>
    <% } %>
    </ul>
```

```js
    var tpl = require('fitemp');
    var result = tpl.render(id,{
      year:	['Shu','Niu','Hu','Tu','Long','She','Ma','Yang','Hou','Ji','Gou','Zhu']
    });
```

Features
--------
    
### include

```HTML
    <div class="parent">
      <%=include('son.html', {[[params..]})%>
    </div>
```

> use filename to change include relative path to absolute path(just like ejs)

> can pass params by include,what is not a function in ejs 

### layout

```HTML
    <div class="parent">
      <%=include({filename: 'sonhtml', layout: 'layout.html'})%>
    </div>
```

### layout.html

```HTML
    <div class="container">
      I'm a container
      content is inside me
      << body >>
    </div>
```
> use `<< body >>` to tell fitemp to put content here

Installation by npm
-----

    npm install fitemp

In HTML
------

```HTML
    <script src="./fitemp.js"></script>
```

	


