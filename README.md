# squared.css

A light-weight css library for simple web design

The library was made using CSS3 so it would surely work on all modern browsers. It is suitable for web developers who wants a simple and light-weight website that could be built very quickly, beginners can also use this library to learn html easily.

[view example](http://arlora.co.nf/projects/libs/squared/)

## Usage

### Initialization

Pass a class name to the selector to initialize the plugin. Elements with the chosen class name will be targeted on scroll. 

```js
$(document).ready(function() {
  $('.example').scrollClass();
});
```

### Set classes to elements

Add the `data-scroll-class` attribute to any element/elements that you wish to target and set a class name as the value.

```html
<div class="example" data-scroll-class="my-class"></div>
```

In the example above, `my-class` will be added to the class attribute of the element when it enters the viewport. (Multiple class names can be added to the data attribute.)

##Plugin Options

- `delay`: Target an element after x number of milliseconds. Adding a delay is recommended for better performance. `20` is set by default. Set to `false` or `0` to disable.
- `threshold`: Target an element when x percent of it is visible in the viewport. Works when scrolling down or up. `50` is set by default. Do not add a percentage sign when setting the threshold.
- `offsetTop`: Number of pixels to offset elements from the top of the window. Useful when a page has a fixed top navigation bar. `0` is set by default. 
- `callback`: Fire a callback after an element is targeted.

Initialization example with all options set:

```js
$(document).ready(function() {
  $('.example').scrollClass({
    delay: 20, //set class after 20 milliseconds delay
    threshold: 50, //set class when 50% of element enters the viewport
    offsetTop: 80, //height in pixels of a fixed top navbar
    callback: function () { //fire a callback
      console.log('Callback fired!');
    }
  });
});
```
##Example
[View Example](http://arlora.co.nf/projects/libs/squared/)

##Contributions

Kindly report any bug to be fixed in the comment issue.

If you want more features, feel free to let me know in the comment issue, or simply add a branch where you can add some feature as well as adding a description on the change so that it could be processed further. 

