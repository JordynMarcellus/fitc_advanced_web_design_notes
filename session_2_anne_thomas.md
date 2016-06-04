**Images are a bottleneck to performance**

GOAL: excellent visual experience across all devices

Designers love huge, impactful images

There is a cost - cost in bandwidth, cost in size. 

Want high quality (imgs) across devices 

* Variety of devices to consider
* users no longer only use desktop to show/work
* Some people only have access to mobile phone

**People will purchase things with their phone**

Reducing load times:

* images not render-blocking but still impact UX 
* non-resized imgs will drain data plans
* necessary to load massive image? fuckity no. 

Fast, good and cheap -- you get two.

Go to img types - jpg, png, svg, gif 
Raster graphics: 
JPG - no transparency, lots of colours, 
PNG - become very heavy very fast (if no transparency, use a fuckin' JPG)

Vector graphics:
SVG - created by math; can be scaled up and down, maintaining sharpness/

Motion graphics:
GIF - can get super heavy, supporting transparency and nimation

GOAL: smallest file size
**Masking???**

#The future of image file types

Hundreds of image file types:

* FLIF
* BPG (but only with some JS - not there yet)
* WEBP (0only owkrs in Chrome & Opera)

Fun to play with, but we're not there yet.

Use progressive enhancement to use `<picture>` element to see if thiese file types are supported

#FAST!!!

##Get help

* Try using a CDN instead of hosting on yr own serer
* AWS, MaxCDN, CloudFlare, Rackspace Cloud Files, CacheFly, AWS

##Caching (saving your images)

* Cach images; change request headers of your resources to use caching
* Edit .htaccess file (if yr rocking that WP or... w/e)
* **Be aggressive**
* Aggressively cache; set long caches for stuff that's not going to change

##Final question: do you really need that many images?

Maybe? Maybe not? 

#GOOD!!!

##Resize those images

Need different sizes of images; CMS can provide options for diff. image dimensions.

* Shopify: upload image as large as you want, max size it uses is 2048x2048;
* WP: you can set diff. image sizes based in functions.php
* Task runners: in PS, Gulp(?)

Ensure different image sizes: 

* kitten-large.jpg (2048 x 1356(?) );
* kitten-large.jpg (1024x768);
* kitten-medium.jpg (640x480);
* kitten-small.jpg (320x240);

##New friends (attributes and elements)

* srcset (new img attr) -- supported in everything but IE (not Edge) and Opera Mini 
* sizes (new img attr) -- 
* picture (element)

###Srcset

* attr added to img element
* allows us to add commas-separated list of diff. images with info about their dimensions
* Possible to specify width of image in relation to browser window or pixel density

Pixel density
`<img src = "kitten-large.jpg" srcset="kitten-xlarge.jpg 3x, kitten-large.jpg 2x, kitten-medium.jpg">`

Width
`<img src = "kitten-large.jpg" srcset="kitten-xlarge.jpg 2048w, kitten-large.jpg 1024w, kitten-medium.jpg 640w, kitten-small.jpg 320w">`

###Sizes

* example syntax for sizes media condition: sizes="(min-width: 769px) 25vw, 100vw"

* Translates to - if viewport is wider than 769px, then image will take up 1/4 of viewport. Otherwise, it will take up the full-width of the viewport. 

###Picture element

* wraps around img element
* append classes to img element (or figure)
* allows for progressive enhancement - if webp is supported, use it instead 

`<picture> <source srcset="kitten-large.jpg" media="(min-width: 769px)"> <source srcset="kitten.webp" type= "image/webp"></picture>`

These allow for art direction. 

#CHEAP 

Not necessarily about money, but about JS we can use to make responsive images across devices.

* automate tasks
* use small amount of JS to make life easier
* cross-browser support 

##Automate resizing

* user-upload images ressized on the fly -- adaptive-images.com or squuezr.it
* task runners to automate image resizing: grunt-responsive-images, gulp-responsive 


#IE/Opera Mini

Picturefill polyfill. github.com/scottjehl/picturefill

Quite a few JS libraries for responsive images

* github.com/kvendrik/responsive-images.js
* github.com/wentin/REsponsifyJS

##LazySizes

* github.com/aFarkas/lazysizes
* combines cross-browser support of srcset and sizes with lazy loading
* have to polyfill for IE (github.com/aFarkas/lazysizes/tree/gh-pages/plugins/respimg)

#Final thoughts:

* educate client on side-effects of large images
* dont' let yourself be constrained to text only
* start using srcset, sizes and picture toda - the more they are used the quicker browsers will implement the desired functionality
* **Fast! Good! Cheap!**

#tips

* strip metadata, lossy vs. lossless
* learn more about design and image editing
