### CSS-Box Shadow

##### What did I want to learn and why:
I was going through the freecodecamp.com course when I came across the CSS box-shadow property. The task was just to copy and paste the property and value into the online text editor on freecodecamp.com website. I was trying hard to understand what it does and how the values work. Like most other CSS-property, the value was not consistent so I had to open another tab and find out more about CSS box-shadow property.


##### What challenges did I have learning it:
The values for the property can range from just one to six values and more if it is nested(shadow on another shadow)
Below are examples of the property value varying size:




##### What I learned and built:
The pattern I observe is as follows:
When only one value is given, it is usually one of these global keywords



Inherit {box-shadow: inherit;} This value Inherits the box-shadow property from its parent element.

{box-shadow: initial;}, {box-shadow: none;}  and {box-shadow: unset;} sets the property to its default value.

When two, three or four length values are given, the first two will represent the horizontal-offset and vertical-offset and the next two will represent the blur-radius and spread-radius. The other two values are optional, which are the inset keyword and color value. To specify multiple shadows, a comma-separated list of shadows can be provided to achieve this.

{box-shadow: horizontal-offset vertical-offset}
horizontal-offset - which is a length value for setting a horizontal distance from the element box. 



A negative value will set the shadow to the left of the element while the positive will set the shadow to the right of the element.

vertical-offset - which is also a length value for setting a vertical distance from the element box. 

A negative value will set the shadow above the element while the positive will set the shadow below the element.

blur-radius  - the third value in the diagram below is the blur-radius

This shows that even if both offsets (first two values) values are zero the shadow is behind the element and still generates blur effects. This is also the same for spread-radius.

The larger this value, the bigger the blur, so the shadow becomes bigger and lighter as shown above. 

Any negative values of the blur-radius will remove the shadow effect on the element

spread-radius - This is the fourth length value. 


Positive values will cause the shadow to expand and grow bigger, negative values will cause the shadow to shrink as seen below. 

If not specified as we have been seeing earlier it will be 0 and the shadow will be the same size as the element.

Inset The inset keyword changes the shadow from being drop shadow to one inside the element box, above the background but below the content with respect to the length values as shown below:


color
If the color is not specified as we have been seeing in earlier examples, the color used will depend on the browser - it is usually the value of the color property which is the default in the above examples.


Here the color property is set to red and hence have the box-shadow color as red as it is not specified, but when the color is specified as shown below, the box-shadow color changes to that value.



