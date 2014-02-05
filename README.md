huge
====
For this task, I created a simple 3-collumn responsive page with a slideshow image that is also responsive. 
I was going to use hisrc.js for handling my responsive  but chose to hand roll a solution for that. You can find that in the  script block at the bottom of my index.html.
I chose to manage the responsive images myself from scratch because I didn't have time to work out the quirks in hisrc. The approach I have chosen is simple and it solves both the 'Art Direction Challenge' (allowing us to provide different images for mobile that are better suited for portrait screens from landscape oriented images for desktop and tablets), as well as being very easy to add to images (just add a 'responsive' class).

Alternative approaches I've seen include having a server-side generate scaled images on demand. I wouldn't use this approach because it will create a lot of unnecessary load on the server for content that's not uniquely generated for each visitor. I would much rather have the images scaled on publish to the various supported sizes and using my approach, request the required size.
In my approach, I have created subfolders for each supported size so the files are organized.
I did not generate scaled images for the 3 columns. In practice, I would have responsive images for those as well and not scale images up as I'm currently doing.

I have 3 breakpoints (<=768, 769 - 1024, > 1024) even though I only had to use media queries for the mobile version. I have a responsive image for the 1024 version though and I'm handling that in my solution.

In my handler for the window resize event, I am using a setTimeout to prevent the script from acting on every pixel change in window size essentially waiting till the resize is complete. Firefox fires this event for pretty much every pixel vs the behavior in chrome and IE which is after the resize is complete.

I did not fully comprehend the requirement for the autocomplete textbox. I had questions on whether you were expecting an autocomplete search box for content or searching a smaller defined list of options (eg. states), so that is not implemented.
