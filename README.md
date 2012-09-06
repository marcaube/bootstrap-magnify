# bootstrap-magnify

`bootstrap-magnify` is a small js plugin to enhance porte-folios and image galleries. It was inspired by [this pen]
(http://codepen.io/scott23/pen/akKqc) on CodePen.io. I try to follow bootstrap js-plugin ethos but keep in mind that I'm
not a good javascript programmer, so it's likely a bit messy.

## What it does
This plugins adds a magnifying glass to images on mouseover. This is useful in porte-folios when you want to show
details of your creation but you don't have the layout space to display your 1200px wide image.

The images used are large images, shown at a smaller resolution on the website, the magnifying glass shows a small part
at the native resolution. Keep in mind that large images are heavy and you must not abuse from this technique.

![Screenshot](https://raw.github.com/marcaube/bootstrap-magnify/master/example/screenshot.png)

If you want to show the large preview at a 200% ratio, just use an image twice the size of it's container.

## How to use it in 3 easy steps

### 1. Add the styles
Import the css file in the head of your website

``` html
    <link rel="stylesheet" href="bootstrap-magnify.min.css">
```

Or import it at the end of your bootstrap.less file

```less
    // ...

    // Magnifying glass
    @import "bootstrap-magnify.less"
```

### 2. Add the script
Import the script at the bottom of your page, after jQuery.

``` html
    <script src="js/bootstrap-magnify.min.js"></script>
```

### 3. Call the script
Now, there is two way you can trigger the functionality. The easy-way, which requires zero lines of javascript is using
the data-api. Just add `data-toggle="magnify"` to your image like this:

``` html
    <img data-toggle="magnify" src="image.jpg" alt="">
```

Or, you can call it manually in javascript like this :

``` js
    $('.container img').magnify();
```