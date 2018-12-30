---
layout: post
title:      "rails project"
date:       2018-12-30 13:48:00 +0000
permalink:  rails_project
---

The rails project can be quite the undertaking, but it is also super rewarding when you hit the home stretch. There is a lot going on at this point. Just going through the rails portion of the curriculum, I remember thinking -- "this is really involved." With the rails project, you are basically building an application or website from scratch. 

For those of you who have not hit this point, there is now a project planning session with an instructor prior to beginning. I found this to be pretty helpful. The prep session forces you to sit down and really think out your project before you begin. I created an outline that basically broke my app down to controllers, models and views. When I got started, I had a roadmap or outline that I was able to reference and keep me on track throughout the project. 

One thing that I found particularly interesting was the scope methods. For my planning session, the scope methods were just a throw-in. I had no idea what they were going to do, and I only included them to check a box off the list. At this point, however, they have added a pretty cool feature to my app. I ended up adding a lot of seed data -- one of my models includes over 100 items. I was able to use really simple scope methods to sort and list my data neatly on the pages. Here is an example of two of these: 

``` 

scope :list, -> { order(parameter: :asc) } 

scope :item, -> { where(parameter: "attribute")} 

``` 

The first method allowed me to list all of my seed data, using one specific parameter to order the data. The second method allowed me to group like items in separate lists throughout the application. When you look at the examples, they don't seem like much, but they really helped me to clean things up! 

As I mentioned, this has been a long haul for me. I am, however, really happy with the result. I already have ideas about how my application could be improved with the addition of some javascript, so I am ready to hit the ground running on the next section. 
