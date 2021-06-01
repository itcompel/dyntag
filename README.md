<img width="100" height="100" src="https://github.com/jsdom/jsdom/raw/master/logo.svg" alt="dyntag"><br>

# DynTag

## Dynamic HTML tag builder for Node.js

*dyntag* is a javascript HTML tag builder for node.js application. It allows you to create any HTML tag dynamically in your node projects. I believe it is the smallest tag builder in node.js environment. 

If you need more features or you have any question about it, you are welcome. 

###Features
- Support Standard all HTML tags
- Dynamic form element [continue developing]

###Installation

    $ npm install dyntag
	
Or globally
	 
    $ npm install -g dyntag


###Usage

First create a dyntag object
```javascript
const dyntag = require('dyntag');
```

Create a html tag without any property
```javascript
dyntag.tag('h1', 'Hello World!').outerHTML
```

Create a html tag with single property
```javascript
dyntag.tag('h1', {class:'title'}, 'Hello World!').outerHTML
```

Create a html tag with multiple property
```javascript
dyntag.tag('h1', {class:'title', id:'main-title'}, 'Hello World!').outerHTML
```

Create html tag with inner tag
```javascript
dyntag.tag('h1', {class:'title', id:'main-title'}, '<p>Hello World!</p>').outerHTML
```

If you use express.js in your project then use it like:

```javascript
app.get('/', function (req, res) {
    res.send(dyntag.tag('h1', {class:'title'}, 'Hello World!').outerHTML);
})
```


###License
DynTag is MIT licensed.
