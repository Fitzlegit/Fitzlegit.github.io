---
layout: post
title:      "Redux, Part 1 (Components)"
date:       2020-04-30 11:17:27 +0000
permalink:  redux_part_1_components
---



React in and of itself can be daunting learning but adding on top of that, Redux can create a
(╯°□°)╯︵ ┻━┻ moment, a couple of them… particularly redux being introduced as a whole can create some mysticism but I promise it’s simpler than it looks… 

We have a few moving parts let’s break them down into components and their roles play in using Redux.

* **Store** — our centralized state this is where we’ll “store” all our data for access for various components… *note: this is a function you’ll need to import into your index.js via redux library and set up through the imported component Provider via the react-redux library.*
 
*  **Input Components** — this is where we enter in our local state data and prepare it to be sent to our centralized **Store**
 
*  **Container Components** — this is where we’ll access our **Store** and assign it to any child component
 
*  **Stateless/Presentational Components** — this is where we’ll display anything that’s been passed down from the **Container Component** (parent)

*  **Actions** — this will hold all your actionable directives(its behavior is similar to a MACRO) in order to connect with the **Reducer**

* **Reducer** — this is where the magic happens, it’s where we integrate/manipulate the data we’ve sent over from our input into the **Store** and return it ready for our **Container** to grab and pass down to any child in the Container…* note: a unique piece about the reducer is every time it’s hit it’ll refresh the state similar to how a local setState function works*

Let’s have a look visually of what we’ve talked about so far

![](https://miro.medium.com/max/2000/0*sMyWxmC7bnvixsYT)
Ex. Redux Component Structure

**Conclusion**

Here, I’m strictly talking about components with the exception of the store, as we move through this series of blogs I’ll talk about the functions needed to get things up and running, show some examples and each individual component inner workings.
