---
layout: post
title:      "Sinatra Project"
date:       2020-01-21 08:18:58 +0000
permalink:  sinatra_project
---


Sinatra brought back some nostalgic memories working with CSS and HTML. For my project, I built out a recipe book - trying to simplify and bring all those years of recipes lying around into a single database using the awesome power of Active Records! 

With a lot more tools to work with this time around, I found this project very pleasant. Generally, when I start a project I like writing out a narrative of what the user can do with the application on paper,  then list out the needed information for the user to be able to do these different tasks. 

After having a rough idea I created MySQL tables for the User and Recipe model, established the relationship type they'd have throughout the application and moved onto working with routes. I separated my controllers into three; Application, User and Recipe controller. I ran into a few challenges here with the understanding of how to set up the configure method and the secret_session which I ended up doing some refactoring by having my other controllers inherit methods from just one application controller. This definitely helped to make things a bit more DRY.

The routes concept didn’t really create too much of a challenge as the CRUD; create, read, update, delete concept was clear and concise. It was though really fun seeing how to apply the logic for sessions and protecting your routes from other users accessing the different user’s information. 

What ended up taking the bulk of my time was working with the CSS and getting pages to be relatively responsive, with just some searching it’s amazing how many different approaches there were to tackle the different challenges that CSS and HTML posed. All in all, I found this project a lot of fun and while I ran into challenges here there, with a little grit and research I found myself solving the problems as they came and getting a better understanding of ruby gems like Rack, Tux and ActiveRecords and several others.
