---
layout: post
title:      "Sinatra: Simple yet Refined"
date:       2020-02-20 04:54:13 +0000
permalink:  sinatra_simple_yet_refined
---


 It is interesting that when we have an open slate, how much harder it is to create something. When allowed to develop anything you want, it seems you want to organize everything and nothing.  How does one think of ideas without overwhelming one with ideas? That is the curse of not having a definitive direction. That was the curse of my second project in Sinatra.

It started easy enough as this was my second project in Flatiron's online web development curriculum. I felt more confident in my abilities with this project than with the Ruby CLI project. The project is closer to the development I want to do and have done in the past.

**The requirements are: **

Build an MVC Sinatra Application.
Use ActiveRecord with Sinatra.
Use Multiple Models.
Use at least one has_many relationship.
Must have user accounts. The user that created a given piece of content should be the only person who can modify that content.
It would be best if you validated user input to ensure that the wrong data isn't created.
Any validation failures must be shown to the user with an error message.
So with all the background information out in the open, I decided what topic to code. I looked from within and find something that I genuinely enjoy and build an app around it. My love of wine was a natural choice. I am a level 1 Sommelier and have enjoyed tasting great wines for years. Why not try to create something that will save those reviews and show me other reviews as well. The Winelister was born out of that thought process.

The flow of the app is the reviewer can see reviews of wines at the start, then will sign up to be able to review wines. Those reviews are added to the overall list but are saved on the reviewer's wine list. The system then allows a person always to have a list of wine reviewed, and another list of other wines to try. The reviewer can add wines, edit their wines, or delete them from the list if they don't want them on.

The app sounds easy to do but has some complexity for a new programmer like me. Based on Flatiron's list of requirements and also just common sense, I needed to add to the complexity. I want to break down three things that I found challenging, then show you how I set the app up, and finally discuss my feelings about the project.

The first level of complexity was allowing users to sign up, sign out, and of course, sign in. While this is pretty standard, you need to make sure forms are working correctly, the views show correctly, and the user is adequately redirected once done.

The second level of complexity was making sure that a person could only take action on their additions. This is accomplished by checking the current user versus the user's params. If they didn't match, then they are not allowed to make any additions, changes, or deletions. This also had to hold for many different levels like user information, review information, and wine lists.

The third level of complexity was making sure that people's information was secure. When a person logs into the app, they need to know their password information is decrypted from the public. Bcrypt was enabled to make sure this happened. 


**MODEL**

I created three model classes: User, Course, and UserCourses
As an instructor, a User has many Courses.
As a student, a User has many UserCourses where UserCourse is a join-table that stores User-Course relationships.

**VIEW**

At the root of my views, I created the layout, login, welcome, and sign up. The layout handles both the header/navigation and the footer. Login and sign up are obvious ones not needing explanation. The final is the welcome screen, which is the main home page when someone is not signed in. 

My views are then grouped based on users and winereviews. I added a third view, which is winelists, but that is a stretch goal for me in the next few weeks.
I mainly set up my crud (create, update, read, delete) in the winereviews class. 

**CONTROLLERS**

I have three main controllers in use with the winelist controller as part of my stretch goal. The application controller inherits Base, which allows me to set up helpers for the rest of the app. I also enabled my sessions and session secret to encrypt passwords. The next controller is my UsersController, which inherits from the ApplicationController. The User controller defines the routes that are relevant for users of the app like login, signup, and an index of all users. The final controller is the winereviews controller. This controller directs all reviews and forces the user to be signed in to post. Once signed in, the reviewer can add, edit, or destroy their reviews only.

That wraps up my blog post explaining my second app for flatiron school. I enjoyed the Sinatra experience as it started to get into more HTML and design attributes. While the backend is essential, I would instead like to work on frontend aspects.The content of your blog post goes here.
