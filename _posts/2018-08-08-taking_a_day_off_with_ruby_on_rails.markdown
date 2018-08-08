---
layout: post
title:      "Taking a Day Off with Ruby on Rails"
date:       2018-08-08 15:32:05 +0000
permalink:  taking_a_day_off_with_ruby_on_rails
---


For my Rails assessment, I decided to rework my Sinatra project using Rails. I figured carrying this project idea throughout the curriculum would show not only how much I have learned and have advanced in my thinking but also give uniformity to my work that makes comparing various languages and frameworks easier.

## Understanding "has_many :through" 

I've always found that throughout the course, the second you feel comfortable and understand something, a curveball is thrown that makes you question how you even got this far and whether or not you know anything at all. My experience with "has_many :through" is a perfect example of this. After countless labs on the concept like the Doctor, Patient and Appointment lab, I truly thought I understood the relationship. Applying it to my project however had me very confused. The assigment required that we had a "has_many :through" relationship and that the JoinTable had an attribute other than the ids of the other two tables. Utilizing my Days Off App idea from Sinatra, I had a Users Table, a Days Table and for the JoinTable, a Requests Table that had an attribute of :reason. "Reason" was a string inputted by the user logging their day off. First and foremost, my Sinatra project with only two tables, meant that users were logging days. Now with the JoinTable, users were actually logging requests for days. Wrapping my head around having a form_for a resource that was a JoinTable seemed unheard of to me and had me second guessing a lot of my code. Jenn helped me understand why it was we would use Request and not Day but getting over the initial confusion and anxiety was a process.

## The Fat Controller: Confusion and Delay

I have fallen in love with the partials that Rails allow. As an Australian child during the 90s, I grew up with *Thomas the Tank Engine* and The Fat Controller, I never thought I would be so obssessed with a **skinny controller**. (Terrible pun, I'm sorry) Alas, The Fat Controller was known for "confusion and delay", a very apt parrallel of skinny controllers that clear up both confusion and any delay.  Private methods have become my best friends. Being able to refactor code and keep things DRY has also reiterated that I am learning and retaining a lot. Partials require finesse and skill, being able to DRY up code is certainly a testament to how far I've come from the days of redundant code. My code now uses before_action methods and helper_methods to eliminate repeated code and also allow for a faster and smoother running code.

This project has taken much longer than I anticipated and hoped but as always life gets in the way. The upside however has been that I can leave Rails knowing that I understand it very well and am confident writing it. I've always maintaing throughout this course that it was not so much about finishing in a timely matter and making sure I just keep passing labs and assessments, but rather that I truly understand the code I write and read.
