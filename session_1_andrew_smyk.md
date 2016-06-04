#Andrew Smyk: responsive design: past, present and future

www.andrewsmyk.com/advancedrwd

Looking @ responsive web design trends from the start to end. 

Watch with floppy disk lol

Gmail didn't work on old-ass iMac; neither did the newspaper sites.
 - some JS and some CSS
 - lesson learned: all you need is HTML.


The old days: screen sizes: 640x 480 & 800 x 600

Now we've got: 640x 480, 800 x 600, 1024 x 768, 1200 x 900, 1920 x 1200

##THE FLASH DAYS

( smyk still uses Flash?! )

##Screen sizes in the year of our lord 2016

There's a whole fucking lot of them by wot. 

Designing for 1.5" (Apple Watch) to 32" (and beyond -- TVs are the next big front-end experiences)

Smart devices (Apple Watch, smartphone) to TVs (can get a 138" TV)

Not only smart devices, but also toys (WITH BROWSERS AND CHAT BUILT INTO 'EM) and dump phones.

Greyscale monitor toys :|

Aspect ratios are important!
 - 5:4 (16:10)
 - 4:3 (16:9)

Samsung device sizes: 2.8" to 10.1" + wearables and tablets.

###Media queries

Average CSS file up to 80kb, which are loading right onto a phone :S

#Designing with text only:

helps keep media queries as simple as possible

Use progressive enhancement to add CSS and JS as you go.

**Unstyled HTML page is ubiquitous and device agnostic**

Responsive typography

Building hierarchy with text
	- size
	- weight
	- color
	- position
	- type contrast

#Modular scale: 

Foundation has modular scales 

Modular scale goes up or down (3/4ths scale)
	- example: 9, 12, 16, 21, 28, 37, 50, 67, 89

Identify content by font size; crates typographic rhythm

Why : increases readability, legibility, balances whitespace and typgrahic texture and provides type contrast

Example scales: 2:3, 3:4, 

##Modular math for 3:4 example
3/4 = .75

16 / .75 = 21
21 / .75 = 28 
(etc)

Users are able to identify content much easier when JS is disabled and the like. 

##Double rail

For another device you can use another font-size and modularize it from there

So, base font on smart TVs is 24
13 / .75 = 18
18 / .75 = 24
24 / .75 = 32
32 / .75 = 42
(etc)

##Modular line height
As screen gets smaller, incrase line height
1/.75 = 1.3

Nintendo DSi as edge case.
- memory allocation blocks; can't modify this at all. 
- DSi browser is Opera Mini :S
- DSi recognizes media queries, but not HTML5 styling elements (strong, em)

