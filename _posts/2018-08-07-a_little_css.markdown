---
layout: post
title:      "a little css..."
date:       2018-08-07 17:27:47 +0000
permalink:  a_little_css
---

Coimng into the HTML/CSS section, I had a pretty good idea of the scope of these tools, but I did not fully appreciate the options offered by CSS. Sure it is easy to spot a basic selector such as:

```
p {
   color: black;
}
```

But what if you want to style a specific id or class? No problem, CSS has got you covered. Let's say that the featured content for a website includes an id equal to "promo", and you want to bold the text in that section. You can use the id selector by placing a hash symbol infront of the id name:

```
#promo {
  font-weight: bold;
}
```

However, let's say there are multiple promotional sections and each has it's own title. The promotional titles have a class attribute, "promo-title".  You can use the class selector by placing a period infront of the class. This would allow you to do something like change the font-size for all of the titles.

```
.promo-title {
  font-size: 2em;
}
```

From these basic selectors, there are plenty of more advanced options, such as compound, descendant, child, and sibling selectors. One of the more complex of these is the attribute selector, which allows you to select an attribute and its value.  Let's say we had a website with dozens of pictures of cats and dogs. All of our cat images have a default "alt" tag of "cat" and all of our dog images have a default "alt" tag of "dog". 

```
<img src="images/cat1.jpg" alt="cat" title="The First Cat">
<img src="images/cat2.jpg" alt="cat" title="The Second Cat">

<img src="images/dog1.jpg alt="dog" title="The First Dog">
<img src="images/dog2.jpg alt="dog" title="The Second Dog">
```

We can use the attribute selector to make sure that all of our cats have a specific border, and all of our dogs have their own specific border.

```
img[alt="cat"] {
  border: 1px solid red;
}

img[alt="dog"] {
  border: 3px dashed blue;
}
```


These are obviously some of the most elementary applications of CSS. The ablility to understand and manipulate selectors is key to being able to create basic websites, including tasks such as styling the page layout and adding responsive features. 

Flatiron's [CSS Fundamentals](https://github.com/learn-co-students/CSS-Fundamentals-v-000) lesson  includes the [CSS Diner Game](http://flukeout.github.io/) as an extra learning resource. I highly recommend this to anyone looking to learn more about CSS selectors.  

