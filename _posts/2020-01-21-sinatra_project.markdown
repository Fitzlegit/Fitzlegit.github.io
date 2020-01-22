---
layout: post
title:      "Sinatra Project"
date:       2020-01-21 03:18:59 -0500
permalink:  sinatra_project
---


Sinatra brought back some nostalgic memories working with CSS and HTML. For my project, I built out a recipe book. I tried to simplify and bring multiple years of recipes lying around the house into a single database, using the awesome power of Active Records! 

I had more tools to work with than I had with my previous project of building a CLI with just Ruby.  So, I found working with this project almost pleasurable.  Generally, I start every project idea on paper, first writing out a narrative of what the user can do with the application; then I make a list of the information needed for the user to be able to do these different tasks. 

Following the rough idea phase, I created my SQL tables for the User and Recipe model, then established the type of relationship they would have throughout the application. More on that later, because the magic of relationships didn’t come into play till much further into my project.  

           Working with the routes was the next step in my process.  I separated my controllers into three:   Application, User and Recipe controller.  I ran into a few challenges here with understanding setting up the configure method and the secret session. I ended up doing some refactoring by having my other controllers inherit methods from just one application controller. This helped to make things a bit more DRY.

The routes concept didn’t really create too much of a challenge because the create, read, update, delete (CRUD) concept was clear and concise. It was really fun seeing how to apply the logic for sessions and protecting your routes from other users accessing the different user’s information. 

What ended up taking the bulk of my time was working with the CSS and getting pages to be relatively responsive.  It’s amazing how many different approaches there were to tackle the different challenges that CSS and HTML posed.  All in all, I found this project a lot of fun. While I ran into challenges here and there, a little grit and research solved the problems as they came.  I feel that I am actually getting a better understanding of Ruby gems like Rack, Tux and ActiveRecords; and several others.


What ended up taking the bulk of my time was working with the CSS and getting pages to be relatively responsive, with just some searching it’s amazing how many different approaches there were to tackle the different challenges that CSS and HTML posed. All in all, I found this project a lot of fun and while I ran into challenges here there, with a little grit and research I found myself solving the problems as they came and getting a better understanding of ruby gems like Rack, Tux and ActiveRecords and several others.
