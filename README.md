![image](https://rawgit.com/Paul-Browne/lazyestload.js/master/demo/images/lazyestload.png "Lazyestload.js logo")

load images only when they are in (and remain in) the viewport. 

in only about 350 bytes of javascript :scream:

```html
  <img class="lazyestload" src="images/placeholder/sunset.jpg" data-src="images/sunset.jpg" >
  
  <script src="js/lazyestload.min.js"></script>
</body>
```


[demo lazyestload](https://rawgit.com/Paul-Browne/lazyestload.js/master/demo/lazyestload.html) load images only when they are in the viewport (or within 100px) *and* when the user has stopped scrolling (meaning the user can scroll past images and they wont be loaded)


[demo lazyload](https://rawgit.com/Paul-Browne/lazyestload.js/master/demo/lazyload.html) load images only when they are in the viewport or 100px beneath


When using placholders the image should be less than 1kb, ~40px wide, and should have the same aspect ratio as the image that will replace it. (to avoid any layout jank) Also the "blur up" affect in the first demo works by adding the following css.

```css
img {
    transition: filter 0.3s;
}

img.lazyestload {                
    width: 100%;
    filter: blur(8px);
}
```
