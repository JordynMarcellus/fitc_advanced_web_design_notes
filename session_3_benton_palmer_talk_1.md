#CSS Layout techniques: replacing floats with flexbox

the beauty of flexbox ;-;

Flexbox is changing how grids and layouts work on the web today. 

Laying out elements in HTML and CSS has changed in the twenty-odd years of web development

##The holy grail layout:

Heading, left column, right column, middle column, footer

Doing this all in tables 

Challenges with this: designers were involved. But what designers like and what can be done in code is... annoying. 

**Flexbox has solved so many fucky CSS layout problems :D :D :D**

*high performance images O'Neill book*

Flexbox is "smarter" in how it counts elements inside the flexcontainer

##Flexbox primer

###Parent flexing
Making something a flexbox container requires the parent to get a **display: flex** css prop

This is the flexbox example we'll be using 
```
.container {
	display: flex;
	/* flex-direction: row;
	flex-direction: row-reverse; 
	flex-direction: column;
	flex-wrap: nowrap;*/
	flex-flow: row nowrap;
	/*justify-content: flex-start;
	justify-content: flex-end; 
	justify-content: center; 
	justify-content: space-between*/;
}

.box {
	
}
```

With wrap, the more elements we insert into the parent container the more we "squished" they get. 

We can use flex-flow as a shorthand to set the direction and wrap properties. 

Flexbox has a couple axes, with top, left, and right being three. 

Justify-content will allow you to set the content's beginning to the start (left) or to the end (right) or... YOU CAN USE IT TO CENTER SHIT

Space-between justifies it to the space between the elements (very nice grid)
space-around does it to the spacing AROUND the elements

```

.container {
	display:flex;
	flex-direction: row;
	flex-wrap: nowrap;
	flex-items: flex-start;
	/* flex-items: flex-stretch || flex-end || flex-end || center; */
	align-content: stretch || space-between
}

```

###Child flexing

####Order property
You can use an order property to set the ACTUAL order of the elements. 

This is relevant to responsive because we can use the order property to re-order elements.

Throw this is in a media query... and suddenly you can have things that on mobile should look one way but on desktop another way 

https://developer.mozilla.org/en-US/docs/Web/CSS/order

####Flex grow

Looks at other children and grows the element based off a factor given by the flex-grow css property

https://developer.mozilla.org/en-US/docs/Web/CSS/order

So, basically, you grow an element by a factor of the css property in relation to its sibling elements

**EASY. RIGHT**

####Flex shrink

Like flex grow but shrinky-dinking

####Flex basis

Give it a width (%age, width) and flexbox will set the element you've set to it to have a width and re-calculate the sibling elements to work that way. 

####Flex 

The flex shorthand property will allow you to set the GROW, SHRINK and BASIS. 

#Accessibility 

Re-ordering can be a little screwy with a11y and flexbox. 

#Support

IE: 10-11 has partial support, <=9 none at all. 

Some are supported with vendor <prefixes class=""></prefixes>