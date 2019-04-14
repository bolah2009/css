# CSS-Box Shadow

## What did I want to learn and why

Am writing about the <abbr title="Cascading Style Sheet">CSS</abbr> shadow box I learnt about few days ago.
I got across this property while learning about CSS on freecodecamp.com before and had to implement it on a project I did both individually and with my coding partner at Microverse.

I was trying hard to understand what it does and how the values work. Like most other CSS property, the value was not consistent (varying number of value).

The values for the property can range from just one to six values and more if it is nested (shadow on another shadow)

Below are examples of the property value varying size which hard different effect:

```css
.shadowone {
  box-shadow: 10px 10px;
}
.shadowtwo {
  box-shadow: 10px 10px 5px;
}

.shadowthree {
  box-shadow: 10px 10px 5px 5px;
}
.shadowfour {
  box-shadow: 10px 10px grey;
}
```

![Alt CSS Box-shadow example 1: Image with four different types of CSS box-shadow property values (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555220024/blog/css-b-s/1.png)

## What I learned and built

The pattern I observed about the CSS box-shadow property is as follows:

- When only one value is given, it is usually one of these global keywords

```css
.shadow {
  box-shadow: initial;
}
.shadow {
  box-shadow: none;
}
.shadow {
  box-shadow: unset;
}
.shadowfive {
  box-shadow: 10px 10px 5px;
}
.inherit {
  box-shadow: inherit;
}
```

![Alt CSS Box-shadow example of when a single global value is provided in this case 'inherit' (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555221745/blog/css-b-s/5.png)

* `{box-shadow: inherit;}` This value Inherits the box-shadow property from its parent element.
* `{box-shadow: initial;}`, `{box-shadow: none;}`  and `{box-shadow: unset;}` sets the property to its default value.

When two, three or four length values are given, the first two will represent the _horizontal-offset_ and _vertical-offset_ and the next two will represent the _blur-radius_ and _spread-radius_. The other two values are optional, which are the `inset` keyword and _color_ value. To specify multiple shadows, a comma-separated list of shadows can be provided to achieve this.

`{box-shadow: horizontal-offset vertical-offset}`
horizontal-offset - which is a length value for setting a horizontal distance from the element box.

```css
.shadowsix {
  box-shadow: 10px 0px;
}
```

![Alt CSS Box-shadow example on horizontal-offset with positive value (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555227656/blog/css-b-s/6.png)

A negative value will set the shadow to the left of the element while the positive will set the shadow to the right of the element.

```css
.shadowseven {
  box-shadow: -10px 0px;
}
```

![Alt CSS Box-shadow example on horizontal-offset with negative value (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555228519/blog/css-b-s/7.png)

vertical-offset - which is also a length value for setting a vertical distance from the element box.

```css
.shadoweight {
  box-shadow: 0px 10px;
}
```

![Alt CSS Box-shadow example on vertical-offset with positive value (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555229454/blog/css-b-s/8.png)

A negative value will set the shadow above the element while the positive will set the shadow below the element.

```css
.shadownine {
  box-shadow: 0px -10px;
}
```

![Alt CSS Box-shadow example on vertical-offset with negative value (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555229454/blog/css-b-s/9.png)

blur-radius - the third value in the diagram below is the blur-radius

```css
.shadowten {
  box-shadow: 0px 0px 24px;
}
```

![Alt CSS Box-shadow example  (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555229927/blog/css-b-s/10.png)

This shows that even if both offsets (first two values) values are zero the shadow is behind the element and still generates blur effects. This is also the same for spread-radius.

```css
.shadoweleven {
  box-shadow: -10px -10px 24px;
}
.shadowtwelve {
  box-shadow: -10px -10px 48px;
}
```

![Alt CSS Box-shadow example of the spread-radius value showing the difference between a small and larger value (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555230088/blog/css-b-s/11-12.png)

The larger this value, the bigger the blur, so the shadow becomes bigger and lighter (or more blur) as shown above.

>Negative values are not allowed for this value. This results in an error and invalidates the box-shadow property

spread-radius - This is the fourth length value.

```css
.shadowfourteen {
  box-shadow: 0px 0px 0px 16px;
}
```

![Alt CSS Box-shadow example of the spread radius value  (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555230531/blog/css-b-s/14.png)

Positive values will cause the shadow to expand and grow bigger, negative values will cause the shadow to shrink as seen below.

```css
.shadowfifteen {
  box-shadow: 10px 10px 5px 5px;
}
.shadowsixteen {
  box-shadow: 10px 10px 5px -5px;
}
```

![Alt CSS Box-shadow example showing two different values of the spread radius property, one positive and the other is negative (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555230531/blog/css-b-s/15-16.png)

If not specified as we have been seeing earlier it will be 0 and the shadow will be the same size as the element.

`inset` The inset keyword changes the shadow from being drop shadow to one inside the element box, above the background but below the content with respect to the length values as shown below:

```css
.shadowseventeen {
  box-shadow: 10px 10px 5px -5px inset;
}
```

![Alt CSS Box-shadow example of the inset keyword value  (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555230990/blog/css-b-s/17.png)

_color_
If the color is not specified as we have been seeing in earlier examples, the color used will depend on the browser - it is usually the value of the color property which is the default in the above examples.

```css
.shadoweighteen {
  color: blue;
  box-shadow: 10px 10px 5px -5px;
}
```

![Alt CSS Box-shadow example our the color value of an element influence the shadow color (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555231295/blog/css-b-s/18.png)

Here the color property is set to blue and hence have the box-shadow color as blue as it is not specified, but when the color is specified as shown below, the box-shadow color changes to that value.

```css
.shadownineteen {
  color: blue;
  box-shadow: 10px 10px 5px -5px green;
}
```

![Alt CSS Box-shadow example  (associated code is above).](https://res.cloudinary.com/bolaah/image/upload/v1555231295/blog/css-b-s/19.png)

## Common application of CSS box-shadow property

CSS box-shadow is used mostly for navigation bars and button. Examples of projects I applied box-shadow to is below:

1. New York Times Clone - Navigation bar - [View in browser](https://bolah2009.github.io/nyt-clone) - [View on Github](https://github.com/bolah2009/nyt-clone)

2. Mint.com’s signup page clone - Button - [View in browser](https://bolah2009.github.io/mint-clone) - [View on Github](https://github.com/bolah2009/mint-clone)

3. Footer link Hover effects - [View in browser](https://bolah2009.github.io/tnw-clone) - [View on Github](https://github.com/bolah2009/tnw-clone)

Here are some resources if you want to learn more...

1. [CSS Tricks](https://css-tricks.com/almanac/properties/b/box-shadow/)
2. [W3Schools](https://www.w3schools.com/cssref/css3_pr_box-shadow.asp)
3. [MDN web docs](https://developer.mozilla.org/en/docs/Web/CSS/box-shadow)
