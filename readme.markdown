# JavaScript Tags Input Library
Native JavaScript library to make **Tags Input** Element in DOM.
There isn't any dependency for this library, add it straight in your project and you'r ready to go.

### Install via npm
```bash
 npm install vanilla-tags-input
```
### Import In ES6 or Greater
```javascript
import TagsInput from 'vanilla-tags-input'
```
### Require in Node
```javascript
let TagsInput = require('vanilla-tags-input')
```
### Import Styles
```css
@import '~vanilla-tags-input/tags-input.css'
```
##3 Alternatively, you can use a CDN or even download
```html
<!-- Tags-input CSS -->
<link rel="stylesheet" href="https://unpkg.com/vanilla-tags-input/tags-input.css">

<!-- Tags-input JavaScript -->
<script src="https://unpkg.com/vanilla-tags-input"></script>
```

# Usage
`Selector` is the only compulsory option to making this plugin work, and it accepts **ID** of input field you want to convert to **tag input**.
```javascript
var tagInput1 = new TagsInput({
    selector: 'tag-input1',
});
```
However there are few other options too like
* **Duplicate** - Set it to yes if you want to allow duplicate tags
* **Max** - Limit the maximum number of tags to be added in plugin
```javascript
var tagInput1 = new TagsInput({
    selector: 'tag-input1',
    duplicate : false,
    max : 10
});
```
## Options
Add multiple tags programatically
```javascript
tagInput1.addData(['PHP' , 'JavaScript' , 'CSS'])
// or add single one
tagInput1.addTag('React');
```

Check if there are any erros to add a tag
```javascript
tagInpu1.anyErrors('another tag');
```
Destroy the instance and release the cached memory
```javascript
tagInput1.destroy();
```
Reinitialize the plugin if previously destroyed
```javascript
tagInput1.init()

// you can reinitialize options
tagInput1.init({
    selector: 'other-tag-input',
    duplicate : false,
    max : 10
})
```
Method chaning available too
```javascript
tagsInput1.init().addTag().addData().destroy().init()
```

## License
[MIT](https://opensource.org/licenses/MIT)
Copyright (c) 2013-present, Yuxi (Evan) You


## For Learning Purposes
Here is a [Demo on codepen](https://codepen.io/iamqamarali/pen/qyawoR)

Find [Tutorial](https://codingfacts.com/create-pure-javascript-plugin/) on how i build this javascript library.
