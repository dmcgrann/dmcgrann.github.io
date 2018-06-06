---
layout: post
title:      "My First Coding Project"
date:       2018-05-24 16:14:45 -0400
permalink:  my_first_coding_project
---


As I write this post, I believe that I am about ready to submit my CLI GEM project for final review, and its been a long time coming. I started at Flatiron on January 3, 2018, so my progress has been on the slow side. In February and March, I was only able to work about 10 hours per week at best. So needless to say, I was pretty excited when I started the project, and I am even more excited that I have a working application. All the same, it took a little longer to move through the project than I ever had anticipated.

My educational background is in liberal arts. It would seem that historical research is a far cry from coding, but that are comparisons... there are always comparisons when it comes to learning. In a liberal arts program, if you are assigned a research paper, you need to come up with an idea, an argument and evidence to support that idea.  A lot can change when you are compiling that evidence. Your argument could simply be wrong or even just a bit off base. You could find that the evidence doesn't quite support your idea or argument. You could find that your argument has been covered to the point that your research paper is now a literature review. Or you could discover that there's no available research materials that support your idea or argument. You have spent all of this time outlining a paper and researching, and now, you are back at square one with the clock ticking on a deadline.

I found myself in a similar place with the CLI GEM project. I spent a few weeks going over ideas in my head. Eventually, I decided that I just needed to commit. My thought was to create an app that would allow students in a specific program choose a list of courses and then choose to view more information about courses. It seemed good to me at the time. I quickly realized that my research paper had turned into a lit review. As I went back through lessons, planning how to build my code, I realized that I had just done similar scraping exercises with courses and students. Oh well, I decided to press on.

I had a little bit of trouble sorting out how to create an environment and sort through the require statements, but I eventually figured that out. I decided to use the "config" folder with "environment.rb" file because it seems like a good way to stay organized. Then I set up a CLI class and a call method so I could test things out, and now I was ready to scrape.

I watched the lessons and read over the examples countless times. I also checked around for other sources of information, and as I mentioned, I went back through the scraping lessons. I set up some basic scraper methods, and they worked well enough in pry that I thought I was on my way. Then, I watched another lesson, and I learned about the challenges of scraping table data. All of the data on my website was table based. Worse yet, a lot of the data was sourced from other places. There weren't many nodes or unique identifiers to work with. In sum, my evidence seemingly did not support my argument.

At this point, I changed course with my project. I chose a new page on the same website that looked to be a bit easier to work with, and I ran a number of tests to see what kind of data that I could actually scrape. In the end, I created an app that collected information for one academic program to be easily viewed in one place. The app allowed a user to choose between the overview and contact information, and it will also provide a list of courses and a list of faculty. This was pretty basic stuff, but it did not really statisfy the objectives of the project.

I decided to take a few days off. 

When I came back to the project, I wanted to see if the issue was the website or the code, so I looked at a course list at a different university. The html on this page was completely different, but I got the same results. This was actually really helpful because I realized that my code was the issue. I went back to my original page, and when looking at the inspector, I realized that I had not gone deep enough with my scraper method. I also revisited my solution to the student scraper lab. I borrowed from this and created an array of hashes for my course information. After a quick meeting with my instructor, I was able to write methods to make all of my objects work together. I now have an app that provides a list of courses; users can select a course from the list, enter another selection, return to the menu, or quit. While still basic, this is more in line with my goals for the project.

My first coding project served as a good reminder that learning is hard but rewarding. As expected, I learned quite a bit about Ruby while working on this, but there were also a few other practical takeaways: 1) work at comfortable pace 2) use all available resources  3) talk to people 4) don't forget to practice self-care.



