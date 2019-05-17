# First-Code-Challenge

This past week I was able to complete my first coding challenge for a company that makes landing pages for advertisers. I would be a Front-end Developer and be able to work remotely, which is a huge win for me. The challenge was to re-create the the layout of a website that they send to you as an image, and the constraint was no frameworks like bootstrap or react were allowed. I love the frameworks out there but their is something refreshing about going back to basics when coding. Writing plane Jane code can be tedious but you get better connected to the language and understanding the bigger picture, and when you are ready to go back to the sweet frameworks you have a deeper appreciation for all the abstraction that goes on. 

## Some Challenges
Some of the challenges I faced when accomplishing this task came when attempting to make my layout responsive with breakpoints and a collapsible Navbar. I needed some of the nav items to disappear at the breakpoint while keeping the navbrand, a button, and a little menu button. When the menu button was clicked the nav items that previously collapsed would be listed in a dropdown.

First to get the items to disappear I added a class to only the items I wanted to hide and in the media query set the display to none. This worked to hide the items but I needed away to show them when the menu button was clicked. First I set the layout the way I would want it to look when the dropdown was active, then added a class of `show` which would only appear in the media query and when the button was clicked. Plain old javaScript in a script tag made this achievable, and by writing a function that selects an element by id and checks the elements class then adds or removes the `show` class to that element. This gives the dropdown a toggle effect. 

One other challenge I had was when the dropdown was active it would push all of my other content down, and mess it all up. To fix this problem took a little research and I had to add a whole slew of css. Basically I had a `div` tag with a class of `collapse` that had children and grandchildren tags. It also had a parent `div` which was a container for the rest of the navbar excluding the navbrand. The key to the correct functionality came by setting the position to absolute and then by setting `top`,`left`, `right`, `transform` with `translate3d()`, and `z-index: 1000`. Some fine tuning to get the right position will be required but it works and moves with its parent element. It looks like this:
```
#css

display: block;
position: absolute;
will-change: transform;
top: 0px;
left: 0px;
transform: translate3d(0px, 50px, 0px);
right: auto;
left: auto;
z-index: 1000;
background-color: #752dd1;
border-left: 1px solid;
border-right: 1px solid;
border-bottom: 1px solid;
border-radius: .3rem;
```

I am grateful for the opportunity to be considered for this job and show my skills. I got to learn a lot of new tricks and got closer to the bare roots of css and html!
