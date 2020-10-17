---
layout: post
title:      "Do I need Redux?"
date:       2020-10-17 08:30:17 +0000
permalink:  do_i_need_redux
---


In my final project for the learn.co curriculum, I need to make a react app that uses redux. I find this interesting because it is hard enough to learn React, then you have to throw in another helper? Nothing like wondering if you are doing the react framework correctly in the first place, then have to include another library to increase complexity. First, I will try in layman's terms to explain redux. Then I want to point out when you need to use redux. From there, I will explain why redux would be a good option. Let's get started...
 
 The official documentation explains redux as a predictable state container for Javascript apps. That, though, isn't really in layman's terms. Further along, it states that it helps you write applications that behave consistently. That is a little better. React is set up, so that parent components pass down props to child components. That is generally just fine with most apps. What happens if you have an extensive app? Communication between two components that don't have a parent-child relationship is discouraged. 
 
 What does that mean? Let's take the family concept. Suppose we have an extensive family with eight brothers and sisters. Those eight families all have four children. Most would agree that it could be a large APP! Well, how do the cousins communicate? Through the parents, but that is fraught with errors and complexity. That is where Redux comes in! Redux is like a family messenger that allows all members to communicate easily one to one.
 
 So when do we use redux? Great question, and let me give you a few answers. 
 
 The first reason to use redux is when you need to use the state globally. The convention of redux is to store the entire state of the application in a single global object. An example of this is when a state change happens in component A it is then relayed to the Redux store, and other components ( D and E) that subscribe to that store get notified of this change.
 
 The next reason to use Redux is when you are passing too many props. In many cases, you may be giving props to a higher-level component using only a couple of those props. It is easier to refactor your props through redux and then send what is needed.
 
 Finally, if you require the state to be mapped between components, an example of this may be the session state after the app loads. The user can be shared between components easily on each page.
 
So what are the benefits of using redux in the examples above?

The state becomes predictable. Redux becomes the one truth throughout the entire application. The store, as it is called, ensures that it is a predictable outcome. This makes it easier to maintain and code.

Part of this predictability is because Redux has stringent guidelines. As Dan Abramov has stated, Redux has pretty strong constraints and limitations. These rules are put into place, so it is predictable across the entire application!

Lastly, because of predictability and the very strict guidelines, redux becomes very easy to maintain and test. There is a common logic and way that all redux applications act, thus become easy for someone to debug and keep going.

Well, this was a basic overview of using Redux with React. I have had a fairly hard time getting to understand why we would want to use it. This was by no means an in-depth discussion but a brief explanation and a little guidance for those who want to know what it does.
