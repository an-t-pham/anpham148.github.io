---
layout: post
title:      "JavaScript Project - InnerWitch App"
date:       2021-03-18 17:41:07 +0000
permalink:  javascript_project_-_innerwitch_app
---


For my JavaScript Project, I've decided to create a single page application for tarot reading.  After spending months to learn Ruby, honestly I've been struggle a bit to learn a completely different language with different syntax like JavaScript. Even though, JavaScript is not as magical nor elegant as Ruby, I've learnt to appreciate how they work, especially DOM manipulation. 

InnerWitch is a fun project because I'm always interested in fortune telling, the art of tarot reading and mystical things like this. So I think it would be a perfect project for a single page application. So when you get into my application, you can either pick the Card to represent your day or pick 5 cards from the deck to have a full tarot reading. 

There are Card and Reading model in the application. Reading has many cards and Card has many Reading. So ReadingCard model is the bridge between them (belongs to both Reading and Card). So I created a getter method in Card so that Card.all will be shuffled randomly and it will be send to front end to determine how many cards will show to the user. 

Hence, I've got a problem that the page wouldn't load because of a promise that the card need to be fetch and render. I need to use `async function` to `await`for my random cards array to render.  Thanks to this, I really appreciate how asynchrony works in JavaScript which actually make all of our social media experience so seamlessly nowsaday. 

Overall, it was a challenge to create a single page application. I've learnt so much about JS, even though I think my knowledge is still very limited. One more project to go to the finish line. I can't wait!

