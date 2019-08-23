---
layout: post
title:      "Don't Sleep on React-Bootstrap"
date:       2019-08-23 16:18:07 +0000
permalink:  dont_sleep_on_react-bootstrap
---


The react-bootstrap framework can quickly take your application from looking like terminal output to looking like a real-life, responsive application. Let's get started.

First, you should visit [https://react-bootstrap.github.io/] and at least skim the documentation. Once you are ready, you can add the package to your project:

```
npm install react-bootstrap bootstrap
```

Now that you have this great tool at your disposal, how can you use it? I will provide two quick examples of how i used bootstap to improve my app: 1) to create responsive navigation, 2) consistent form styling.

If you aren't a fan of the menu on the react-bootstrap site, you can always turn to google and search, "bootstrap-react [item]," and quickly find documentation. The bootstrap site not only spells out the features, but it also basically provides the code. When I got started, I already had a very minimally styled navigation bar (it was at least pinned to the top of the screen). In order to update this, I first imported the bootstrap files to my NavBar component.

```
import { Nav, Navbar } from 'react-bootstrap'
```

I included the Brand feature to add a logo, and Toggle and Collapse to make the NavBar responsive. In my original set up, I used react-router-dom's Link to link to locations. Bootstrap's Navbar includes a link feature as well, so I was able to remove react-router-dom from this component and rely on bootstrap. In the end, my code looked something like this:

```
import React from 'react';
import { Nav, Navbar } from 'react-bootstrap'

const NavBar = (  ) => {
  return (

    <Navbar collapseOnSelect expand="lg" bg="dark" variant="dark">
      <Navbar.Brand href="/">Test App</Navbar.Brand>
        <Navbar.Toggle aria-controls="responsive-navbar-nav" />
        <Navbar.Collapse id="responsive-navbar-nav">

              <Nav.Link href="/sales">Sales</Nav.Link>
              <Nav.Link href="/sales/new">Sale Form</Nav.Link>
              <Nav.Link href="/map">Map View</Nav.Link>
              <Nav.Link id="logout" href='/logout'> <Logout /> </Nav.Link>

  </Navbar.Collapse>
</Navbar>

```

You do have the option to customize the style. For example, if you look at the example above, you can change the "bg" and "variant" attributes, based on your preference. You can also take this a step further and update your stylesheet. I wanted my menu links to be red, so I added the following: 

```
a.nav-link{
  color: red;
}
```

You have to be careful though because when the screen is reduced, the resulting hamburger menu will retain the default coloring. Without getting into great detail, I needed to update the default settings to remove the glow effect when the hamburger icon is clicked, as well as update the border and text. This is captured in the following: 

```
button:focus {
    outline: 5px;
}

.navbar-dark .navbar-toggler {
    color: red;
    border-color: #626D75;
}
```

In the end I had a black navigation bar with red link text, and a grey hamburger icon (when collapsed).

I'd also like to briefly discuss react-bootstraps form options, which include disctint styles for different inputs. I used bootstrap forms somewhat extensively, but the user attributes provide a good example. I used bootstrap to style my email and password components. Again the first step, import bootstrap.

```
import {Form}from 'react-bootstrap'

```

Then I used boostrap's elements to create reusable email and password components. This came in handy because i had separate signup and login forms. A really quick look at this:

```
import React from 'react';
import {Form} from 'react-bootstrap'

const EmailInput = props => {

    return (

        <Form.Group controlId="formBasicEmail">
          <Form.Label>Email address</Form.Label>
          <Form.Control type="email" placeholder="Enter email" {...props} />
          <Form.Text className="text-muted">
          </Form.Text>
        </Form.Group>
    );
}
export default EmailInput;
```

...and...

```
import React from 'react';
import {Form} from 'react-bootstrap'

const PasswordInput = props => {
    return (

      <Form.Group controlId="formBasicPassword">
        <Form.Label>Password</Form.Label>
          <Form.Control type="password" placeholder="Password" {...props} />
        </Form.Group>
    );
}

export default PasswordInput;
```

Form.Group sets the input type (there's also options for text, checkbox, etc.), while Form.Control includes basic formating. 

With just these few elements set, I was able to plug these components into my form components, and create separate forms that retained the same look. Much like with the NavBar, I also updated the stylesheet to position my forms accordingly.

There's obviously much more that bootstrap can do, and I encourage you to take a look at the url in the introduction. You might not use the bootstrap framework throughout your entire application or website, but it can be a great asset to help enhance certain features.
