---
layout: post
title:      "CLI Project"
date:       2019-12-16 03:35:12 +0000
permalink:  cli_project
---


The CLI project took me a bit through the wringer, originally the concept was fairly simple in my head but started to produce a few funky problems throughout the time spent on it. I wanted to create a CLI that displayed the information for Paste’s Magazines top 100 anime movies and return some data based on the user requests but I quickly realized the site didn’t quite meet the requirements nor was it strictly HTML. That led me over to IMDB which had the same information setup in a fashion that I could scrape multiple levels for the information I was looking for.

Quickly I broke the process into about three different parts after identifying a rough idea of what I was planning to do, wrote my object attributes I would be scraping out on paper and some simple pseudo-code of how my CLI would run. Having a rough draft I was ready to begin.

Sidenote:  When using the learn IDE, I cannot stress enough just how important it is to,

```
git add .
git commit -m “some text”
git push 

```

Now with a blueprint for the project, I began creating my ruby gem CLI through the gem bundler. The bundler created a bit of an unfamiliar file naming structure that hadn’t been brought up much in the lessons... 

> Quick tip: When naming your ruby gem at creation using the bundler though kabab-case seems to be the preferred casing for project names, bundler will create a subfolder for each “-” so be sure to use snake_casing and make the change before digging into your project.

> Quick tip 2: The old familiar environment file that we’ve seen so often in our labs, I’m sure you’re wondering where that went! That’ll have the same name as your lib subfolder, sitting directly in the lib folder. Be sure to change that too if it’s confusing.
 
After taking care of that and properly sitting up the environment I moved onto scrapping with nokogiri gem. Scrapping can be done in a few ways, I choose the “harder” way the first time for my own purposes of understanding the CSS selector method. I recommend spending a few hours with the nokogiri documentation and scrapping some simple sites to get a handle on it.

Combing over and following the selector paths for each section I was able to use the class names to return information in the block. That brought up a small problem though, a few of the blocks didn’t have a defined class name making it impossible to scrape information in that manner. Luckily nokogiri is more flexible than that. There were two methods in which I could solve this problem; one, iterate through the block to the specific array point since nokogiri essentially turns all your data into arrays and the other magical easy way is simply inspect the element and copy the selector. This was probably the bulk work of the project after having all the information scraped from the site I moved on to developing CLI class and the methods that would govern how it would run.

Building the CLI model and other models were fairly straight forward at this point. I built an anime model that held the object attributes and saved the objects after being created. The CLI model had a few different methods that didn’t take too long to build out and get working, on a side note be sure to brush up on the “gets” method look at a few CLI examples to familiarize yourself the general methods that go into a simple CLI, it’ll help a lot and speed things along.

Overall the project was great for pulling together what I’ve learned so far and apply some core concepts. It was definitely a bit of a challenge to get underway but once coding began I enjoyed building out the whole project.

