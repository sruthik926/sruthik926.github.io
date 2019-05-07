---
layout: post
title:      "Approach to Debugging "
date:       2019-05-07 03:27:35 +0000
permalink:  approach_to_debugging
---


Debugging can be a challenging as well as interesting for a developer. At least, thar's what I experienced during my journey at Flatiron School. I feel that the first step is to think and approach a problem with a calm mind. I think a calm mind helps one to think better and have a clear mind during the problem solving process. I certainly came across error messages while building my Ruby on Rails project. I would read and try and understand the error message as the next step. One of the error messages I came across was "First argument in form cannot contain nil or be empty." I think it's important to read other details on the error page. The beauty is that the error page will also have some info as to where the error is within the code. 

This particular line points you to the specific erb file within your application. "Showing /Users/sruthikrishna/Documents/FlatironSchool/SelfPaced/symp-project/app/views/students/_form.html.erb where line #14 raised:"

Based on this message, I figured out that my error was within my views folder of my application - specifically the students folder under the views folder. I also knew that the error was pointing to line 14 of on my form_.html.erb file. I think these clues help the developer understand the error messages better. I took a look at line 14 of my form_html.erb file. It was pointing to the first line of the form for.

<%= form_for @student do |s| %>

Initially, it took me some time to understand these types of error messages. I also referred to Google/StackOverFlow to figure out what these error messages meant. However, now that I look at it, I think the error message is pretty explicit, It's telling me that @student object that is being passed in through my form for is either nil or empty. The next step would be to figure out the reason for this. Why would my @student object be nil? It would make sense for me to check my controller actions. When I took a look at my Student controller, I realized that my student object was not instantiated. I was missing the @student = Student.new within my new controller action. From my perspective, problem solving involves brainstorming. We may, as developers, may not be able to come up with a solution right away, It definitely requires us to think of different possible solutions. Debugging may only be about programming. However, the problem solving aspect can also be applied to other real world scenarios - the way we think, the way we come up with solutions etc. 








