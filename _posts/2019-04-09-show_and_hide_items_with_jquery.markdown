---
layout: post
title:      "Show and Hide Items with jQuery"
date:       2019-04-09 12:03:14 -0400
permalink:  show_and_hide_items_with_jquery
---


This might seem pretty basic to many, but sometimes the simple things are what we inevitably overlook. While building my rails with js project, I wanted to add a form to a page, but I didn't want the form to always be visible. After a few searches, I stumbled across a great suggestion -- show() and hide(). Again, this seems ridiculously simple, but let's take a quick look.

Basically, I wanted to have a form that would allow a user to select items from a list to add to an object. This list included 119 checkboxes with the potential to be two to three times that length. Obviously, I wouldn't want that list to appear each time a user visited the page. Enter the jQuery hide(). All you need to do is grab the selector you want to hide and it to the function.

```
function () {
    $('#selector').hide();
}
```

With that enabled, the section with that selector will not be visible. Most likely, one would want to have an option of making this section visible. This is easy enough. You can just add a link or a button to the page and use a click event to show the hidden section. For me, it looked something like this.

```
function showHide() {
    $('#form').hide();
    $('#add').click(function(e) {
      $('#form').show();
      e.preventDefault();
  })
}
```

When a user clicks the link with id="add", the form will appear. I wanted to make sure the form is hidden again after it is submitted, so I added a call to my showHide() in the function used to submit the form. While this might not be the most elegant method, it is effective. A user opens the form by clicking the link, makes some updates, submits the form, the new data replaces the old, and the form is once again hidden. And all of this happens wthout reloading the page.

You can find more information about show() and hide() in the [jQuery documents](http://api.jquery.com/category/effects/basics/). This section also includes [toggle()](http://api.jquery.com/toggle/), which might be more condusive to your needs.

