---
layout: post
title:      "React-Redux project"
date:       2019-10-02 01:48:08 +0000
permalink:  react-redux_project
---

I honestly did not think that I would able to pull of the React and Redux project. I wanted to build a price comparison app and specifically wanted to use an external API for it. It took me days to find a price comparison app.  My initial idea was to use individual retailer APIs.  I tried looking up APIs for many retailers such as WalMart, Ebay, Amazon, Target, Etsy and Best Buy.  However, I ran into some challenges in getting access to these APIS.  I could not register as a new developer or either had to be an employee in order to have access to the APIs. I was quite frustrated at that point. Yet, I kept going. I tried not to give up so easily. I was able to sign up for developer accounts with Etsy and Ebay. However, I was not so keen on having just two APIS. I wanted to be able to compare prices among mutiple retailers. I kept searching for external price omparison API. I finally found one that provided information of multiple retailers...yes, all within one API. It got me so excited! I used the PriceYuge API to make my app happen. I guess this was one of my biggest challenges during the React-Redux project process. 

The React-Redux project not only helped me understand React better but also helped me reinforce some of concepts of Rails and JavaScript. I learned how to create multiple components within my app . I also learned that each component has its own set of responsbilities. For example, my app has a Product Detail component. It's responsbiloty is to mainly render an item's specifications or product details. My app has another component named CompareCard Component. The CompareCard component mainly renders the price comparison details of an item. Again, each one(component) has its own functionality. My Product Detail and CompareCard components.are purely presentational components. To my understanding, presentational compoents are just responsible for presenting data. This data can either be props or just hard coded HTML. An item's product details and price comparison details are being passed down from the Item component. All of my data is really being stored in the Redux store...another concept which I really learned.  

I think another importand and beneficial aspect of a component is reusability. I realized that we can use or invoke components within other components. 

I understand that Redux is important for large scale applications. I think I could have created my app without Redux. However, I applied it to my app and learned so much in the process. Redux is typically used to maintain data or state all in one place. Redux is also broken down into different parts such as action creators and  reducers, Thunk is also a very interesting concept. I used Thunk to make fetch requests to Rails server as well as the PriceYuge server. I believe that Thunk is usually used to make asynchronous calls.

I also learned how to integrate React/Redux and Rails. I knew that React was all about the front end and Rails was about back-end. I didn't really see the big picture til now.  I will continue to enhance my price comparison app as it never ends. I would love to put into production at some point. I look forward to building more React/Redux apps.

Here are is a summry of  some insights into how to go about the project

* You will get stuck at different points of the project and sometimes can be quite frustrating- but keep codinga dn playing with the code and try  different options.

* Checking with your peers and friends is also an option to get a very different perspective- this goes both ways so helping them out with their issues is also a great learninge experience.

* Stackoverflow.com is taking it to the global level- You would be amazed at the prompt responses that come in from all over the world.

* At the end, it is an exhausting journey and the excitement on seeing the light at the end of the tunnel is truly rewarding.

* Remember, it never ends and it i sjust the beginning....


