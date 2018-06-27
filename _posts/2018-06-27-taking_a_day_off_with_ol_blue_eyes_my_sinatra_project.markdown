---
layout: post
title:      "Taking a Day Off with Ol' Blue Eyes: My Sinatra Project"
date:       2018-06-27 14:56:07 +0000
permalink:  taking_a_day_off_with_ol_blue_eyes_my_sinatra_project
---

It can be hard getting started on these projects if you aren't inspired, but the idea came to me immediately once I read this line in the README: "The app should be a custom app that is created to track something important to you." I knew right then I wanted to create a web app that logged and tracked days off, because honestly, there is nothing I find more important than a day off, especially given my grueling full time work schedule and this course. 

Right before starting this project, I was put in the Beta structured online FSWD program and my peers in Rake-it-til-u-make-it have been extremely helpful and motivating, not to mention Cernan and Jenn have been tireless in their leadership. Because I was a part of this cohort, I did skip some labs in order to start on the same page as my peers. Although this had me at the same starting point as the others, it certainly put me at a disadvantage as a lot of the elements required in the Sinatra Portfolio Project were covered and cemented in both Fwitter and Playlister, two labs that I had not completed before starting the Project. 

Working through the Project, I kept finding myself getting confused between what would belong in the Users Controller and what would belong in the Days Controller. Jenn explained to me that there is a shift once the user is logging their days. Although the User has many days, the URL will reflect the :id of the day itself and any subsequent actions, i.e. deleting or editing the day, are applied to the day itself.

This project deepened my understanding of MVC. The notion that the Controllers handle logic, the Models handle data and the Views handle the presentation. It was enlightening to see the flow between all three, particularly between the Controllers and the Views. Before deciphering where to place my Binding.pry, I would follow the flow of the site. I would run 'shotgun' in the terminal and wait to see an Error Page or Sinatra Doesn't Know This Ditty. I would then go through the Controller and see where every method led to in order to validate the Error Page that actually stipulated the line of code throwing an error. This helped with my understanding of the functionality of the app itself. I came to realize the immense importance in reading error messages because their hints are often quite helpful, for example, indentifying that something should be an instance variable or highlighting a spelling mistake I missed.

The concept of params had been something I hadn't fully grasped. Utilizing params so much in this project in order to identify the data I needed has helped me understand params a lot better. The vehicle that carries the form data to the Controller. The notion that the keys in the params hash match the names in the HTML. Params being a hash of key/value pairs provided by Sinatra containing information about the web request made. Once I understood that, I was able to use them more effectively rather than guess that I needed to pass in params.

My app Days-off is also the first thing I have created in a local environment. Setup of which was quite difficult and time-consuming but once it was up and running, I didn't miss the Learn IDE at all, despite how spoilt it had made me. Using Atom and the Terminal, apart from making me feel more like a legitimate coder, has also taught me the value in setting up a good foundation, i.e. a config.ru that is ordered correctly in that it mounts and then uses, as well as the value in setting up a Gemfile that has more than what you think you need, like a toolkit that is well stocked and means you're prepared for anything. 

The Corneal gem was an incredible resource in creating my app. The scaffold provided by Corneal actually stubbed out the Controllers. Although it made me second guess my own thinking when I went against it, it was an asset in helping me understand how to order the Controller. The idea that the HTML requests get more specific the lower down in the Controller and that each request is independent of the others in the sense that an instance variable set in a previous method is not defined in another method. A helper method in the application controller can define the instance variable but it will still need to be set in every HTML request. E.g. 

`def current
   @current_user ||= User.find_by(id: session[:user_id]) if session[:user_id]
	 end`
	 
being defined in the Application Controller will still require

`@user = current_user`

in the User and Days Controllers. 

All in all this project was difficult but emphasized that as much as I still believe I don't know anything, a lot has clicked. So much so to the point where I was able to create my own web app with functionality, sound logic, and even security protections- certaintly not an easy feat.

