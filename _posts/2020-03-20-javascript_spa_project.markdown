---
layout: post
title:      "Javascript SPA project"
date:       2020-03-21 02:09:00 +0000
permalink:  javascript_spa_project
---


Every time I sit down to write about a new project and reflect I realize I’ve just scratched the surface in each language. Javascript is deceptively simple in what it does but the massive library makes it daunting.  There are a million and one ways to success and while that may sound excessive, javascript has dozens of solutions for completing a task. 

I decided to migrate this project over from my Sinatra project:  a recipe database/UI online cookbook…  This gave me much needed time to focus on the javascript rather than the CSS and backend. 

Okay, let’s dive into the nitty-gritty! Originally, I had planned to create a user login and what-not but scrapped that idea due to time limitations... My SPA (single page application) had simple user stories (I thought)

* A user can view all recipes in the database
* A user can create and add recipes to the database
* A user can delete their own recipes in the database
* A user could login and view their recipes
* A user could create a personal cookbook
* A user could add recipes to a personal cookbook

I had to scratch a few of those out due to the time constraints, and also the fact that my project code was becoming a lot bigger than expected.

Let’s talk about fetch requests or similarly, AJAX  request.  If you’re stumped there’s far more documentation (easier to find documentation at least) on ajax than fetch.  They differ a bit but generally operate to the same ends.  

One of the differences is its simplified way to deal with CORS (cross-origin requests). I had to do a little digging since when I first started making my requests to the database they would get rejected due to a CORS error. Dealing with GET/POST was easy enough with headers.  However,  when I started implementing my DELETE method I had to grab a gem and just ended up allowing all requests since this is just a local development project. This component was probably the biggest challenge and it still feels as though there’s a lot more to know about configuring fetch requests.

Delete fetch request
```
deleteRecipe(recipeId){
  let configObj = {
  method: 'DELETE',
  headers: { 'Content-Type': 'application/json', 'Accepts': 'application/json'}
  }
  fetch(`${this.baseURL}/${recipeId}`, configObj)
   .then(res => {
     if(res.ok) {
       return Promise.resolve('Recipe deleted')
     } else {
       return Promise.reject('An error occured')
     }
   })
   .then(res => console.log(res))
   .catch(err => console.error(err))
   main.innerHTML = ``
   window.location.reload();
}
```

Using Javascript as an OOL(object-oriented language):  This would’ve been a bit of a curveball had I not already had an understanding of object-oriented languages.  It was still strange how Javascript achieves this by acting in an asynchronous way and then encapsulating data. To separate my concerns I built out a recipe model to handle my recipe constructor and rendering of all my recipes, a recipe adapter to handle my sanitizing and fetch request of my data and then an index which handled more generalized information, such as my menu and form.  I found it a little more difficult to pinpoint structure with javascript after coming off rails and MVC.  I  still feel unsatisfied with the structuring as it seems like the wild west. 

I like javascript for what it offers using the DOM with event listeners and having actions happen without having to reload the site all over again.  But as this is basically vanilla js with rails as an API, I see the limitations when wanting to expand or make my site more robust. The solutions to the problems as they became more complex demonstrated the necessity of having a framework.

