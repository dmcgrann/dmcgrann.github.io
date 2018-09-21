---
layout: post
title:      "Getting Started with the Sinatra Project"
date:       2018-09-21 19:50:24 +0000
permalink:  getting_started_with_the_sinatra_project
---


As I hit the final stages of my Sinatra Project, I thought it might be useful to share a few things that helped me get started and kept me going.

I think the biggest thing for me was the corneal gem, which gives you everything you need to get going. Once you install the gem, you will see a structure that emulates what you are used to seeing in many of the previous lessons.  This includes an app directory (with MCV directories), a Gemfile, a Rakefile, db and config directories, and even a stylesheet. Once the gem is installed, you can cd into your app, run shotgun, and verify that it is working correctly. That's right, your app is already working and you haven't really done anything. Talk about peace of mind. There are a few videos on the Learn video page that walk a user through set up. The video that I watched was about 10 minutes and really helpful. Otherwise, you can find more information at http://rubygems.org.

The next thing was discussed in one of the lessons, but it bears repeating: clear out your database from time to time, or even more often than that. You can clear your database by running rake db:drop. Or you can even just delete the development.sqlite, schema.rb, and test.sqlite files. These files will be regenerated when run a new migration, but don't forget to migrate back into the test environment as well (rake db:migrate SINATRA_ENV=test). Starting with a fresh database helped me to have an easier time testing my code as I went along. 

Similar to above, I also found that refreshing the browser improved my testing. I use Chrome, and I have been bouncing between a Dell and a Mac. In both cases, clearing the cache and cookies before testing made my app run better. Speaking of testing, as we have been continually reminded, read the test carefully. The failed tests generally lead right to the root of the problem.

And lastly, be mindful of typos. I write this mostly for myself, and I can tell you from experience that it can be frustrating to stare a screen and think "...but the code is right?!?!" During the Fwitter lesson, I had all but one test passing. I can't remember which one it was, but it made no sense why it wasn't working. In the end, it turned out that I had typed "nethod" in one of my forms instead of "method." That was a bit embarrassing.

Anyway, working through this project has been both fun and challenging. I am looking forward to the next sections!
