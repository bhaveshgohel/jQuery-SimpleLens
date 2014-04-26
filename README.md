jQuery-SimpleLens
=================

This is a simple script to magnify images.
The files needed to make it work are these:
- src/jquery.simpleGallery.js manages a simple gallery with thumbnails and big images.
- src/jquery.simpleLens.js does all the work for the magnifying of the images.
- css/jquery.simpleLens.css provides the css code needed from the magnifying script.

**jquery.simpleGallery.js is optional and you can use any plugin that does the same thing.**

The demo folder contains all the file needed for the demo.
In the demo.html file you can find some examples.

**The basic html markup to make the lens plugin work**:
```html
<div class="simpleLens-gallery-container" id="demo-1">
    <div class="simpleLens-container">
        <div class="simpleLens-big-image-container">
            <a class="simpleLens-lens-image" data-lens-image="demo/large/benvado_elisa_bianco.jpg">
                <img src="demo/medium/benvado_elisa_bianco.jpg" class="simpleLens-big-image">
            </a>
        </div>
    </div>
</div>
```

**Initialize the plugin like this**:
```javascript
$('#demo-1 .simpleLens-big-image').simpleLens({
    loading_image: 'demo/images/loading.gif'
});
```

**Options**:
```javascript
$.fn.simpleLens.defaults = {
    anchor_parent_class: '.simpleLens-lens-image',
    lens_image_attr: 'data-lens-image',
    big_image_class: '.simpleLens-big-image',
    parent_class: '.simpleLens-big-image-container',
    lens_class: 'simpleLens-lens-element',
    cursor_class: 'simpleLens-mouse-cursor',
    loading_image: 'images/loading.gif',
    open_lens_event: 'mouseenter'
};
```