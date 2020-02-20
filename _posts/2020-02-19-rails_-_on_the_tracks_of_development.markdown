---
layout: post
title:      "Rails - On the Tracks of Development"
date:       2020-02-20 04:58:18 +0000
permalink:  rails_-_on_the_tracks_of_development
---


My third project for Flatiron School of Web Development is to do a ruby on rails project. The key isn't to do any random rails project, though. We have criteria we must meet that shows we are learning development. I set out to complete my ruby on rails Flatiron project with a very detailed plan for an e-commerce site selling Bonsai. Not only could you get the Bonsai, but you could also review them. Lets set out the Flatiron criteria.

First and foremost, the application needs to build a content management system. Ruby on Rails can handle this quite well, which is why it is popular with so many startups.  I am meeting this condition in two ways, first through having a bonsai class (product) that requires content. Second, I have reviews that need management of that content as well.

Our models must have one "has_many" relationships, one "belongs_to" relationship, and two "has_many :through" relationships. The main models I have are User, Bonsai, and Reviews. The Users and Bonsais have a "has_many :through" relationship with each other through Reviews. Reviews belong to both user and Bonsai. Finally, both the Users and Bonsais have a has_many relationship. The models both need validations as well as submittable user content(reviews). 

The next challenge was adding an active record method, which I used when displaying my Bonsais with the .order.

As with most apps, we needed to include standard user authentication with sign up, log in, and passwords. The user can also sign in with Twitter as well. 

Throughout the app, we need to have validation errors for users when mistakes are made. These validations help a lot with the user experience of the app.

Finally, we are not allowed to use scaffolding as it sets up all of the MVC to match. The goal is to make everything work with our own hands, not ruby convention. I also think scaffolding adds a lot of code that is not needed down the road.

As Mike Tyson said, " Everyone has a great plan until they get hit in the face." Well, on this project, rails walloped me and made me rethink a lot of things. I believe organization is key to developing a successful app. My reason for this, though, is different than most. By having that organization, you can move directions easier. You become more nimble and can figure out how to change versus chaos only allows you to go down one path. 

I think another lesson for me on this project is wrapped around the minimal viable product theory. Not that we are releasing this as a product but start small with what is required, and you can add later. Grandiose plans, even well-intentioned and organized, can overwhelm at first. The next project will have stages in them that allow me to be successful right away and then build up from there.  If I were a senior developer and could plan for everything in my head, then this is not a necessity.

Prepare for mistakes. I would tell myself that you will make a lot of errors and not get so down on yourself when you are not hitting self-imposed deadlines. We all have goals, and when something isn't happening as we want, it takes time to work through. What you don't need is the stress of finishing within a specific timeframe to add to what you already feel. We are doing this to learn, and to learn means mistakes have to happen, is what I would tell myself.

Overall it was nice to work with Ruby on Rails because it allowed me a little more freedom with CSS and HTML. The framework is challenging and yet makes sense at the same time. As Mats says, Ruby is made for people, not machines.

I am looking forward to the next project, which has a rails background!
