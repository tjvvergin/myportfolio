+++
title = 'This Website!'
date = 2024-02-23T00:23:01-06:00
draft = false
tags = ["projects"]
categories = ["projects"]
+++
## [Github Link](https://github.com/tjvvergin/myportfolio)
### My philosophy of what makes a good website:
I have always been fascinated with how people use the programs that they do on a daily basis. As a technophile who likes to use programs which both look nice and function well I first considered going into website design when entering college. Website design was my original ambitions until I took some more advanced classes and noticed that it was not the actual user interface but the streamlining of workflows which actually interested me. I certainly still appreciate a well designed website that looks good but if the looks get in the way of funtion I end up feeling more frustrated than satisfied. This would be something that I would keep in the back of my mind when deciding on a website layout.
### Why did I end up using Hugo?
 I looked at options like SquareSpace, Wix and Wordpress but found that they were all very expensive options to keep running and would not be nearly as fun and interesting as trying my hand at creating my own website. I have some minor experience working with JavaScript but not enough to code a full on functioning website using a modern framework. This is why I decided to turn to a static site generator, with the one I landed on in the end being Hugo. From what I read while doing research on static site generators, Hugo stood out to me as a robust option which requires little in the way of advanced web development knowledge with lightning fast build times to make learning quicker and easier. This stood out to me as a great option with the benefit of plenty of themes to choose from and flexible options to change layouts to my liking. Hugo's extensive use of Markdown formatting also made a lot of sense to me as someone who is used to using Markdown in Github repositories. 
### My design decisions.
I knew coming into this that I wanted to make this website reflect me as a person as best I could. To do this I needed a few things from a theme: 
1. I wanted a minimal layout with super simple navigation that could take the user from any page to another. 
2. I also wanted support for simple light/dark themes depending on the users machine. 
3. My last requirement was for a super clean homepage which had a picture of me along with the links to my LinkedIn and Github profiles.

After browsing the themes section of Hugos website I quickly came across Papermod which seemed to take care of all of these requirements easily. This would give me a solid base to start from and would allow me to finally git init my project and upload it to my repository.
## Time to start programming.
After skimming through a [quick tutorial](https://www.youtube.com/watch?v=hjD9jTi_DQ4) that I found online as well as some online documentation done by the Hugo team and the Papermod team I got started with creating the homepage. Something that all of the tutorials recomended was to change the hugo.toml file that it started with to a hugo.yaml file that was far easier to understand and code with. I had some difficulties figuring out how to get hugo to track the .yaml file while building but after a little more research it was done and I could follow along with the tutorials.

#### Built in buttons should be easy right?
I started by using the built in social-media icons and links to link to my Github and Linked-In accounts. From there I copied a picture of myself into the image-url field of the profileMode structure in the hugo.yaml file. When trying to test the basic functionality of the website using the command *hugo server* I got a confusing error message suggesting something was wrong which I could not figure out. After googling the error message it suggested I had made a syntax error which I was not aware of. I was not familiar with .yaml files before this so it took me a little while to figure out that in the code below there needed to be a '-' at the beginning of every new socialIcons field. 
```yaml
socialIcons: 
    - name: "github"
      url: "https://github.com/tjvvergin"
    - name: "linkedin"
      url: "https://www.linkedin.com/in/tyler-vergin/"
```
With the only issue being a missing '-' at the beginning of `name: "linkedin"`, even with working example code side by side it was difficult to notice the difference at first. Solving this would implant an important reminder in my brain for the rest of this project to always pay attention to the '-' in the .yaml files. After doing pretty much the exact same process for the remainder of the buttons on the homepage I could continue on to the other parts of my website. 

#### Creating the list of coding projects.
The next issue I faced came about when trying to only show coding project posts when the user clicked on the "Coding Projects" button or in the toolbar. I had seen examples online of lists and saw that there was a list layout in papermod but could not quite figure out how to get it to work. Every time that I would try to make a page use that layout it would error out. Eventually I was able to figure out that the list layout was meant to be used inside of another layout and was not meant to be standalone. Knowing this was now a dead-edn I went back to the Papermod documentation and figured out that if I just changed the url so that it looked like '/tags/projects/' that it would pull up a list of all posts with the "projects" tag. 

### Finally Publishing the website
Once everything was nicely organized and several pages were filled out I went ahead and published the website. There were several different options but the obvious winner for me, as everything was already in Github, was Github pages. Pages is completely free and managed entirely by Github themselves with seamless integration allowing the website to automatically get updated with the latest main branch version. All of this was made even better by Github allowing custom domains to be linked to the website meaning that [TylerVergin.com](https://tylervergin.com) would officially exist.




