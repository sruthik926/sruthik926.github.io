---
layout: post
title:      "MVC vs Component based Architecture "
date:       2019-08-03 21:19:31 +0000
permalink:  mvc_vs_component_based_architecture
---


When I started my web development journey, I was introduced to Ruby and Rails. I was fascinated with framework and the tools that it provided to build an end to end application using the MVC architecture. The simple routing mechanism along with the Active record based ORM helped a beginner like me stitch together a full blown functional application rather quickly and I was completely in love with this framework.

Soon after, I started picking up the basics of React and the component based architecture . Component based web development is the current rage in the industry- even Angular.js which started off as a MVC based javascript framework, soon switched over to component based in its later versions. Did that mean the end of MVC ? I began to research on this while half way down the React reading material. In the the following sections I will summarize my findings.

* MVC(Model-View-Controller) was the earliest architecture adoption for designing web applications- It provided a way for the application segregate the client and server components allowing for code reuse and single responsibility principle.Most of the popular programming languages had MVC frameworks including Rails and Ruby.

* Soon after, SPA(Single Page applications) became a popular implementation- For users who were transitioning from desktop application with rich UI features, SPA helped provide the same look and feel and eliminated the need to connect to the server and load a new page for data view refresh. Most modern web application fraeworks like Angular and React have adopted SPA principles. The MVC based frameworks relied on hybrid techniques like AJAX or other libraries to implement SPA features.

* Component based web architecture was first introduced with React and Facebook actually introduced it as a Java script extension that served as the "V" of MVC. To me, that indeed did make sense because, one of the nagging questions I had was  "how React dealt with data and if it had a Active Record like tool to interface with the database." It relied on REST API's to fetch the data that it would then render on a SPA(Singe Page Application).

* Some others argue that frameworks like Angular is a component based MVC framework because components are an independent in itself and has the code for view and data in one unit. Realistically, complete reusability  is a challenge because different clients may require different flavors of the same component albeit with minor changes thereby breaking the resusability factor.

* IT leaders argue that component based architecture is the future due it's modular apporach and reuse reducing many of the dependencies that a MVC approach may have. Building resuable components also speeds up the development process. Google moved out of the MVC apporach that it had for the first version of Angular to a component based architecture with later versions.

* One can also argue that the services connecting to the backend is the Model and that the component is a mix of view and controller.

Summary- Component based architecture is certainly the way to build web applications. Whether this means the end of the raditional MVC based frameworks remains to be seen.



Sources 

Alex Moldovan, "Is Model-View-Controller dead on the front end?",  October 9, 2016,  accessed August 3rd, 2019 
"https://www.freecodecamp.org/news/is-mvc-dead-for-the-frontend-35b4d1fe39ec/"

Damien Scott, Mundi Morgado, "6 Reasons for Employing Component-based UI Development View Larger Image",  accessed August 3rd, 2019
"https://www.tandemseven.com/technology/6-reasons-component-based-ui-development/"







