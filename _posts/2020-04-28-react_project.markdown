---
layout: post
title:      "React Project"
date:       2020-04-28 12:08:55 +0000
permalink:  react_project
---


React Project… the final installment of my guided studies at Flatiron school, I can feel the heavy strokes of those words. This project I built out an application for meditation that used React framework as its front end and Rails as an API backend. The front consisted of a few basic features which were the utilization of a count-down timer, a user profile, a list of goals and some statistical data to track the sessions of the user. 

If you followed me up till now ( or not ) the previous project I worked on was building an SPA with vanilla javascript which in my humble opinion was a series of sins I hoped to sweep under the rug and never speak of again, fortunately I had to revisit those challenges to complete this project. 


While React is a powerful tool that certainly creates some ease using javascript through an adapted language jsx it fundamentally runs on the same principles and concepts. 
	
My first challenge was creating users and logging them into the application in order to persist their information and create a personalized experience for each user, simple enough. This was a particularly difficult piece to implement at first, easy to conceptualize but tough to put into practice. I had to expand and deepen my understanding of the use of Redux, Thunk and fetch to get this rolling and I must admit this had me stumped for quite some time… the misconceptions slowly got dispelled as I painstakingly “broke” my application to functionality  to understand each step that was taking place throughout process. On the other side of this when I think about it seems quite simple but in the thick of it I must admit it had me quite stumped to the point that I needed added explanation to get past it.


My second challenge after finishing up with the user login and returning the data came building out a countdown timer, we had built a few timers in the past but because of the logic of how I wished my clock to perform I found myself, working out quite a bit of logic in the code in order to restrict the user input and keep the formatting uniformed throughout the lifecycle of the use. It was interesting because I felt I was putting use what we learned in our first module and dealing with conditionals logic is something that just takes time, here’s snippet of the timer code;


```
  handleOnChange(event) {
    this.setState({
      [event.target.name]: event.target.value.slice(0, 2)
    })
  }

  startTimer(event) {
    if(this.state.isRunning === false){
      this.setState({
        isRunning: true,
        [event.target.name]: event.target.value
      })

      this.timer = setInterval(() => {
        const { seconds, minutes } = this.state


        if (seconds > 10) {
          this.setState({
            seconds: seconds - 1
          })
        } else if(seconds > 0) {
          this.setState({
            seconds: '0' + (seconds - 1)
          })
        }

        if(minutes < 11 & seconds === '00' & minutes > 0 ){
          this.setState({
            minutes: '0' + (minutes - 1),
            seconds: 59
          })
        } else if(minutes > 10  & seconds === '00') {
          this.setState({
            minutes: minutes - 1,
            seconds: 59
          })
        }


        if (seconds === '00') {
          if (minutes === '00') {
            clearInterval(this.timer)
            this.setState({
              isRunning: false
            })
          }
        }
      }, 1000)
    }
  }
```





My next challenge was completing the user profile, this is where I was really able to drive home the understanding of fetch requests to the backend and separate where  actions and reducers came into play. I had built all my profile components at first without combining the reducers, at this time I was simply hitting the backend purely with a fetch but not dispatching an action to the redux store to store the information returned from the backend for use in the frontend. This helped to spread a lot of light on the mechanics as I moved forward to combine my reducers into a root. 

Lastly, there were a lot of small “hills” to overcome but posed the usual challenges that a developer might run into as they build out an application. This project reminds me of when I built out my first Sinatra and Rails projects. It helped to solidify my understanding of ruby and many core concepts that at first were shaky due to the lack of real-world use cases under the limited lens of using the language alone. I’ve begun to really appreciate what javascript has to offer within a framework and look forward to building even applications to further my understanding.

