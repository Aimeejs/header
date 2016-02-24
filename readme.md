# Header

### Install
```
aimee i header
```


### Example
```js
var Header = require('header');
var header = new Header;
header.init().render();
// or
header.init(data).render(id);
```
Or in page
```js
page.exports('header');
// or
page.exports('header', data);
// or
page.exports('header', function(app){
    app.init().render();
})
```


### Skin
skin.less
```css
.lincoapp-header.skin-red{

    h1{
        color: red;
    }
}
```
home.js
```js
var Header = require('header');
var header = new Header;
// 应用red主题
header.init().skin('red').render();
```
or
```js
page.exports('header').skin('red');
```
or
```js
page.exports('header', function(app){
    app.init().skin('red').render()
})
```



### Preview
<img class="shadow" src="source/preview.png" alt="" width="320">

```js
page.exports('header', {

    title: {
        value: '',
        className: 'logo'
    },

    left: {
        className: ''
    },

    right: {
        className: 'ishare'
    }
})
```
<img class="shadow" src="source/2.png" alt="" width="320">

```js
page.exports('header', {

    title: {
        value: '悦图',
        className: ''
    },

    left: {
        className: 'iback'
    },

    right: {
        className: 'ishare'
    }
})
```
<img class="shadow" src="source/3.png" alt="" width="320">
