#haris's talk

Space Jam website. ;-; so beautiful

Ethan Marcotte's first article on "responsive web design"

1. Fluid grids
2. Flexible images
3. Media queries 

Responsive design ecosystem is changing

JS & CSS features, tools, tips and pointers. 

#CSS layouts

Floats & display:inline-block. The bad old days that focus on individual HTML elements.

Flexbox! The new hotness. 


##Flexbox 

Majority of CSS properties in flexbox are applied to container. 

Flexbox is all about the flow of elements (flex children)

* direction
* alignment
* other stuff 

With Flexbox we're looking at a cohesive whole, not individual elements. 

Flex thinking: what width/ratio does (element) need to be relative to its siblings 

Main + sidebar layout -> flex-grow main, flex-grow 1 sidebar

Mobile breaks out sidebar and puts it on top...

###old way
Absolutely positioning shit on mobile like that is horrible. It completely breaks the flow of the DOM 

###flexy way
Flexbox: using *flex-direction: row-reverse*

No flexbox? No problem, use the CSS direction property. 

so you can use display: inline-block and direction rtl (right to left)

**Learn to control content flow**

**Understand the flow of the items you're working with, you'll be able to control things without too much CSS fuckery.**

#Sizing

Sizing units include: %age, em, rem, vh, hw

Mahmood says to really explore these 

Foundation 5 uses ems and rems, Bootstrap does to. 

Using rems, apply a base font-size to the html, then use the rem unit to multiply the html pixel size value. So, 3 rem @ 14px base font-size = 42px

Allows you to use a media query to change the HTML... and you won't have to fuck with more media queries.

**Mahmood says the pixel will die soon enough**

AVOID FIXED MEASUREMENTS + ABSOLUTE POSITIONING AND MAGIC NUMBERS

Fixed measurements - use percentages

Absolute positioning - try to use flexbox, other kidns of positioning

Magic numbers - numbers that are arbitrary that will blow up if that CSS property changes ONE IOTA


#Handling responsive web design at scale

* Create maintainable and organized code 
* Large teams can use these principles to establish best practices

Two recommendations:

1. Preprocessed CSS (Sass, Less, Stylus, PostCSS)
	* Breakpoint mixin
		* allows you to establish a pre-defined set of breakpoints
		* ensures consistency
		* creates discussion and proper maintenance
		* Front-end developers and designers should be friends! We work closely together and are part of the user experience
2. Modular CSS
	* separate into objects and concerns
		* import individual concerns like base styling, some typogrpahy styling, etc
	* keeps all code related to module **together**
3. Object-oriented CSS + BEM -- check out Harry Roberts videos. 
	* CSS architecture

This can lead to better, more maintanable and reusable CSS code. Which is sexier. 

#Mobile? Desktop? Why not all devices? 

Media queries, device detection, device orientation

Mobile device gets hamburger menu in top-left corner.

Google's material design starts to do this more and more. 

**Hiding menu items reduces visibility and impacts UX**

Everything in responsive web design needs a purpose and a reason.

There are many mediocre experiences on mobile, watered-down desktop experiences

This is no longer sufficient. It's harmful to business, harmful to conversions. 

Google's SEO ranking/metrics changed, making mobile-friendly pages rank higher in the search

**GOOGLE AMP**

Mobile-only website technology. This also means you get an HTML tag with a little lightning emoji. 

**Facebook instant articles**

Speed is essential

#Looking ahead to the future

* more amp and instant articles 
* css grid layout 
* Rachel Andrews 
* gridbyexample.com
* web components - little modular elements with scoped CSS to itself (HTML video element is a web component) 
* polymer 	

Responsive web design should be a given on every project, not the final thing to get knocked out near the end of a project.

RWD is an approach to creating websites that **respond to all known web browsing devices** with content delivery and ui interaction optimized to the greatest degree possible **for all visitors.**