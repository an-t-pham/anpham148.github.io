---
layout: post
title:      "My Rails Project: LetSpace App"
date:       2021-01-23 10:38:42 -0500
permalink:  my_rails_project_letspace_app
---


So... I've used the same idea from my Sinatra project purely because there are so many new functions that I can apply to improve my app from Rails. Like nested routes, I can actually create property within a landlord route which made way more senses because properties belong to landlord. At first, I thought oh it will only take me 2-3 weeks to finish this project. Little did I know it took me almost 5 weeks to complete this. However, I've learnt so much in this process. There are a few new things that I wish I knew that would make everything so much easier and quicker. So I hope I would share here for anyone interested. 

1. You can actually name your association or foreign keys yourself because my Property model has many current tenants and previous tenants and they are from different models. Before I knew this possible, I kept changing my association between from one-to-many, many-to-many, one-to-one and none of that seems makes any sense, until I realised this is possible. So you can either check out this article (in source section): https://www.theodinproject.com/courses/ruby-on-rails/lessons/active-record-associations or check out this Rails App Building video: https://www.youtube.com/watch?v=8bP45hcVZaA&list=PLI_-ZfHw8Y6UtkEuZ9aJ-DN3t1L0_8BGs&index=1&ab_channel=JenniferHansen (it's in part 1 when Jennifer first created all the models and routes)/
 

2.  Because of the relationship between my Property model and Tenant model (one-to-one, Property belongs to Tenant & Tenant has one Property); however, sometimes a property doesn't have tenant (it's completely different association with Landlord). The solution is you can put optional: true in Property model. 
```
class Property < ApplicationRecord
    belongs_to :landlord
    belongs_to :tenant, optional: true
```

3.  I've spent 3 days for OmniAuth - google oauth 2 and I've followed every instructions step-by-step but nothing seems work. Until I realised that, I've missed the gem 'omniauth-oauth2' which no article or instruction mentioned about (it's probably because it was 1 year ago file). Also turned out I've to specify the version which is gem 'omniauth-oauth2', '~> 1.6.0'. That's when it works because the latest version 1.7 doesnt work and the older version will conflict. So yes if you have trouble with Google Oauth 2, please consider to check the gem version you've installed.


After all, I'm glad to finish this project and quite proud of this. However, obviously, there are more I could have done to improve the front end experience and more logic could've been applied to make it better. Overall, I learn that it is really important to check the version of gem that you've used and if you follow an article, make sure they are as new as possible. 

