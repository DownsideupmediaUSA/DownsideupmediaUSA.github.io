---
layout: post
title:  "The Final Project : Angularjs"
date:   2017-04-09 19:14:53 +0000
---


So for my final Flatiron Project, I am sticking with the music player theme and this time I'll be using a Rails back-end and Angularjs, along with Semantic which was recommended by our assessment instructor. Semantic is a great alternative to Bootstrap as it seems much easier to get the elements you need into your design. Of course, doing your first angularjs project will come with it's plethora of "curveballs", and deep "rabbit holes", so it was no surprise that I'd find myself asking "did I screw this up already? Setting things up through bower made a lot of easier, even though the Semantic docs didn't tell you how to integrate it into an angular site, but after a lot of digging around, I figured out how to set up dependencies in my bower file to handle all of these external libraries that will be needed for this project.

Working with Angularjs feels like its the combination of Rails and Javascript because essentially it is exactly that. it gives the front end of your site a framework from which you can make a users experience much more enjoyable without the unneccessary of page reloading. From a developers standpoint, it allows you to properly separate concerns and organize the structure of your site, keeping your controllers skinny, while, through the use of services, give your different parts of your application the ability to have access to desired behaviors and functions. This being my first entry into Angularjs, I found the experience to be fairly easy to wrap my head around, perhaps due to my growing experience in working with Rails. 

But back to my application, basically it follows my music theme. This time the site is a single page application where everything happens on the root (or main) page as opposed to loading additional pages. I kept things rather clean and simple as far as design, giving the user the ability to easily navigate to different pages within the application. I utilized a factory to create the objects that represent each track, which essentially grabs the data provided by the active model serializer, which in turn is injected into the DOM(Domain Object Model), or basically, what the end user actually sees. 

Setting up features like the ability to search for various tracks was simple using the super simple ng-model directive and setting it to "searchbox"... that was easy. Getting the likes to update on the page was a little trickier but in the end wasn't so tough. It just involved making and hooking into a thumbs up icon and using the ng-click directive along with creating a function in the cooresponding controller called plusOne which takes in the index of the track, takes the new "like" and is then displayed in a counter that is next to the icon which increments by one for each like. 

Finally I added some validations to a contact form which checks to make sure there is a valid email address. This involved creating a separate service to handle the validation. This function basically takes a look at the email field and if there is either no email address entered or (through the use of some nifty regex) if the email address doesnt follow the standard address format, that an error message is displayed to the user to make the necessary corrections. 

Yes, there is a lot I need to do to eventually make this a functioning application that I can actually use for my own purposes. Jplayer is a js library that will add the ability to play the specific tracks. This sounds easy but it is not. Additionally there are very few tutorials on how to add music players to angular apps that don't confuse the heck out of me but in the end this site needs to have full functionality and I am excited to forge ahead and use everything that I have created here in an application for my music label. 

Onward!
