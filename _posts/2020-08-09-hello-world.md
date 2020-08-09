---
title: "Hello world!"
date: 2019-04-18T15:34:30-04:00
categories:
  - blog
tags:
  - website
  - tech
  - Jekyll
---

I always wanted to have a personal website for multiple reasons unknown to me. It always felt good to have a home for myself in this endless ocean of the internet. From day one I started to think about this seriously, I had certain criteria in my mind which had to be met if this project was to materialize ever. One such criterion was that the site should load as fast as possible, even on a 2G network. That means the website should be static and not dynamic. One-click solutions such as WordPress was not my thing to go for. WordPress sites are easy to set up but it was too heavy for my liking. I chose "Jekyll" as my preferred static site generator for these reasons. It was lightweight, fast and the most suitable for blogs. It gave me the convenience to have a local environment for testing important changes before pushing it to the site. 

Setting up a local Jekyll environment and building a barebone website took just under an hour. It would have been much shorter if I was not distracted by my nephew wanting to play with the mouse. Next up, had to pick a suitable theme for the site. That was not very quick. I had to research a lot for zeroing in on a theme that matches my criteria of being minimal, fast and responsive. Yes, there are a lot of minimal, fast and responsive Jekyll themes out there, but none matched my sense of aesthetic beauty. 

After two days of intense search left and right, ended up choosing a Jekyll theme named "minimal-mistakes". This was exactly what I had in my mind. It checked all right boxes for me and it felt really good to pick a theme that wouldn't compromise with my idea of a fast and responsive website with a "feel good" UI. Setting up the theme was again, a somewhat easy process. It didn't take long - thanks to the excellent documentation provided by the theme author. 

So now I had a website with a nice theme and all the necessary placeholder contents inside. All there was to do was to change the placeholder text to my name. That's it! Hooray - I have a website! Wish it was that easy. Since I was planning for a blog website, having a comments section beneath the posts was one of my primary requirements. ( It's not that I expect anyone to read all the posts and take their time to comment something on it). The minimal-mistakes theme by default supports a bunch of comment providers such as Disqus, utterances, Facebook comments etc. 

Neither of these comment providers was acceptable for me. Disqus was the easiest to set up but it was kind of heavy and slowed down the site. And it didn't match the overall UI of the website. I didn't even bother to try the rest as I knew they all would look like a cuckoo's egg in a crow's nest somehow. Then I noticed that the minimal-mistake theme supported staticman comments. It was baked in by default into the theme and can be triggered by a couple of added line to the configuration page.

Alas! Little I did know at this point. I was quick. Added the necessary lines and pushed the commit and waited for the comment box to magically appear and start working. As you might have expected, it didn't work. Not even the comment box appeared with all the necessary HTML code inserted. What was I doing wrong? Googled and googled for days and days - three days to be specific. Finally, after seeing the possible solution to the issue, I almost felt like banging my head on the wall. Comment boxes won't appear if I am building and testing Jekyll sites locally unless we force the goddamn thing to production mode. ( simply, I had to enter a command to get the comment box to appear offline). So fixing that made the comment box to appear. But now a new issue popped up. I had two comment boxes stacked on top of each other. 

Debugging it took a day more, and finally managed to kick the unnecessary comment box out. All is well and good. Now all I had to do is just to write a comment and click send. And no. It wasn't working. Again googled for a solution and found that the official staticman API was now defunct. It seems a lot of people used staticman API for getting the comments to work and it ran out of limit and simply died - two years ago. So here I was, trying to beat a dead horse ( dead for two years) to get my comments working.


Next possible solution was to host an instance of staticman comments for myself on a cloud hosting provider so that it will serve comments only to my website. I forked the staticman repository on Github, deployed it to Heroku ( a cloud server) and gave the necessary permissions to do something ( honestly I don't know exactly what it does) and make the comments appear on my website. It didn't work either. The official staticman fork was broken. By this time, I got exhausted and planned to ditch this project entirely. I was not willing to settle with anything other than what I imagined my website should be like. Thanks to the one special friend who encouraged me not to leave this halfway, I decided to give it a last shot. Pulled some commits from here and there ( it's not this easy, of course. It reminds me of a joke I read online - why engineers are paid so heavy if all they do is copy code from stack overflow? The answer was something like it's not for copying the code they are paid for, but for exactly knowing which code to copy), merged with the staticman repo, hosted it and checked if my comment robot living in the cloud was alive and kicking. Yes, it was. It greeted me an OK just as I wanted it to.

Next, I had to make my website talk with the comment robot whenever someone posts a comment on the website. ( I was the one who was posting comments such as is this working? Are you dead? What the fuck, appear you asshole comment etc.) This seemed a tougher job than what I had to face with hosting the robot up there in the heavens. The comment box always returned an error. With the network traffic debugged, all I got was an error 500. It took almost a week to get this thing out of the way and one fine day, my comment appeared on the website successfully. It was just like seeing your baby for the first time after birth. This is not an exaggeration but after all the things I have gone through it felt so good. 

Now the result is the website works, the comments work, the reCaptcha works to eliminate spam. I can now post blogs on topics I would like to rant - that could vary from space to spice. Let me wind up this here for now. Peace out comrades!



