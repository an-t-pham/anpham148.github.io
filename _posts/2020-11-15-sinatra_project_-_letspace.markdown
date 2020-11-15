---
layout: post
title:      "Sinatra Project - LetSpace"
date:       2020-11-15 08:00:29 +0000
permalink:  sinatra_project_-_letspace
---

Welcome to LetSpace! This is a Sinatra App to connect landlords and tenants together. 
Before speaking about my project, I have to say how proud I am to have my own little app. Well, it's not perfect but I made it. I still can't believe it!

First of all, I've struggled a little bit to come up with the idea for this project as I don't want it to be too complicated but at the same time not too simple. So then I remembered when I was living in London and being ripped off by letting agents. I thought it would be great if there is an app that can connect landlords and tenants directly. 

The second problem I encountered in this project was the relationship between tenants and properties because obviously properties belong to landlords but does tenants belong to properties or tenants has many-to-many relationship ? So I went down the road with many-to-many relationship because tenants can move a lot so they can have a lot of properties and there can be many tenants in the same property. However, I had to simplify tenants controller because the whole previous tenants and current tenants inside property getting pretty complicated and I already spent a lot of time for my landlord's controllers. I decided to keep it simple. 

My User Story is that landlord  (primary user) can sign up/log in/log out to their account which includes their info and their properties. So they will be able to edit their own account and delete it. They also will be able to view, add property, edit and delete their properties. I also add that they can see all of their current tenants and it would link directly to their tenant's profile but they won't have authorized to see the edit/delete button. I have a secondary user tenant who can also sign up/ log in/ log out to their account which include their info and all available properties in the app. 

I've learned so much about Sinatra after building this app from sessions, flash, CRUD, Active Record and a little bit of CSS, though my CSS skill are still very terrible. I've found Ayana’s complete build series very useful through Sonja Parsell's blog! You can find her video series in instruction videos. Ayana explained so well the sessions, flash and has a complete check list for the project.

Lastly, even though we should have a clear goal in term of minimum viable product, don't be afraid of challenges. Of course there will be a lot of time you get stuck and regret the route you chose but trust me you will learn so much more from your mistakes. Don't be afraid to make them!

Overall, I feel proud and happy of this project even though there is still a lot of aspects that need to be improved!
