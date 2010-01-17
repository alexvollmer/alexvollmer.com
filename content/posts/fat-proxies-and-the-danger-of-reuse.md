----- 
permalink: fat-proxies-and-the-danger-of-reuse
title: Fat Proxies and the Danger of Reuse
date: 2008-02-19 01:50:25 -08:00
tags: ""
excerpt: ""
original_post_id: 65
toc: true
-----
UIs are, essentially, collections of widgets. These widgets act as visual and manipulative proxies between the user and the underlying conceptual model. If we think of the ultimate UI as being one which minimizes the mental distance between what the user wants to do and what they have to do to accomplish it, perhaps the ideal interface would be like the fictional jet-fighter, [Firefox](http://imdb.com/title/tt0083943/). What could possibly be more direct than thinking, fire that missile, and seeing that missile burst forth from under the wing? Unfortunately, since most of us work on slightly less fantastic technologies than those portrayed in the movie, we have to figure how to work best within our milieu. This is the real challenge of what we do. How can we take the crude medium of computer software and diminish the distance between thinking and doing?

Yesterday I checked out a site that plays in the same space as a project I'm working on. These sorts of things are bit like going to the dentist, you don't necessarily look forward to it, but you do it because it's good for you. It's not that I'm trying to ignore what is out there, but for a side-project there is a certain bliss in being ignorant of what else is out there--especially when there really isn't any money at stake. But I was a good boy and checked it out. I went in fearing the worst--that these guys would have nailed the concept and the interface, and there was simply no reason to put any more time on our version. After about fifteen minutes I was pretty convinced that we could come up with a more compelling user experience.

Like mom always said, if you don't have anything nice to say, say it anyway--just don't name names. So let me try to provide some detail on what I found without tipping my hand. This app had all the right rounded-corner-drop-shadow-muted-blue patina that any self-respecting Web 2.0 app should. But digging a bit under the surface revealed a pretty face on what was essentially a Windows for Workgroups-era application mentality. The user flow felt like it was driven from the underlying relational data model, not necessarily from sensible use cases. As I filled out wizard form after wizard form, I couldn't help imagining each one mapping to a particular table in a database. In addition, each form had several tabs with a mix of required and optional features to be identified by the user. The tabs were clearly meant to further sub-categorize the input, however because of the limited real-estate in a tab, only single-word descriptions were available. I had to click on each tab to see if I needed fill anything out in there or not. Too much clicking to satisfy the data model, not enough payoff for the user to keep it up.

Then I ran into something called "templates". I can't help but wonder if templating concepts aren't a smell rather than a feature. In the case of this application, it wasn't really clear what the benefits of templates would be. Normally templates are there to avoid repeating work and providing a model of re-use. Looking at this "feature", I couldn't help but wonder why I should care. If templates are so damn important, do I really want to use an app in which templates are a necessity? Again, too much work, no clear payoff. Humans serve the machine. Bah!

So why would somebody put something like templates in? The answer is re-use. Software developers simply love re-use wherever they can get it. I can imagine the developers and product team sitting around reviewing this complicated system they've built and finally having to address the fact that the complexity makes it hard to use. Templates to the rescue! We can reduce the user's work-load with reuse! Ugh. It's only an economic win if I really care to continue the app. Otherwise the real problem lies in the original interaction model.

The Golden Age of Perfect Software is nowhere on the horizon so building software will continue to be a type of gruesome sausage-making for the foreseeable future. One of the great lies about software development is the false economics of reuse. The theory goes like this: if applications can be built by assembling more-powerful, higher-level components together, the overall cost of software development should decrease. At face value this theory makes a lot of sense. I'm sure many of us can think of time we have wasted (or seen wasted) on building rounder wheels. Why should anyone spend time working on a library of sorting algorithms when for 99.999% of all cases the sorting routines available with your platform are adequate?

The problem is that the component-based thinking doesn't always match the needs of the application. Sure we may have built it more cheaply than if we had written it from scratch, but we have to ask ourselves how much did we compromise in that effort? Software is a notoriously tricky business and the number of failures greatly outweigh the number of successes. Google wasn't built in one shot. Heck, the first version of Google Reader was so badly panned, they threw it away and wrote another one. Apple is on the tenth major version of the OS software and fifth major revision within the latest family. Let's not kid ourselves, we're much more likely to get it wrong than get it right. So let's just assume that it's possible that none of the available, reusable components is going to suffice for your needs. That doesn't have to be your starting assumption, but we have to keep the possibility in the back of our minds.

This leads to a second point I'd like to make about re-use. Many UI toolkits come with a pretty rich array of widgets that are used to build nearly every application out there. This is true of native clients as it is of web applications. If our goal is to minimize the conceptual distance between the user's mental model of the application (remember, the developer's mental model is almost irrelevant) and what they need to do to meet that model, then restricting ourselves only to what the widget palette offers will be fraught with compromise. Developers may see applications built as collections of widgets, but users often don't. It's quite possible that using the "standard" widgets for your application greatly increases the mental distance between thinking and doing for the user. When this happens the user is serving the application--not the other way around. Uh oh. Wrong turn. Back up. Try again.

Don't misunderstand me. I'm not saying that every application has to be written from the ground up because there is no hope in getting the interaction right by reusing off-the-shelf components. That's ridiculous. We'd never get anything done if we approached our apps like that. Rather, my point is that we can't necessarily limit ourselves to the widget sets and conventions of our platforms. In doing so we may leave the user out in the cold. However, visual or interactive exceptionalism for the sake of differentiation invites similar risk. Dressing up your app to stand out is akin to putting lipstick on a pig. If you app is compelling, dressing it up will be unnecessary.

Let's return to our anonymous whipping boy...er, sample web site. Not only did the wizards and multiple-layers of object hierarchy force me to learn the tool's model (one I don't care about), but the expression of those wizards (the widgets) similarly required me (the user) to play along, rather than getting me to the payoff. Some applications are very sophisticated and will require more of the user, but that's not the case for this one. Indeed the selling point is how easy it is to use and how user-focused it really was! Boo, hiss. F-.

So while the wizards had a very consistent and recognizable look and feel to them, they did a horrible job of getting me to where I wanted to be. I can't help but feel that this application was built with a primary focus on a relational data model and component reuse. This ended up with fat proxies between me and what I wanted to get done--an increase in the mental distance between thinking and doing. This is the real shame. Increasing that distance is the primal sin of application design.

One final note: a lot of the inspiration for this post came from a [fantastic post](http://katidev.com/blog/wp-trackback.php?p=20 Computer Administrative Debris) by Cathy Shive on, what she terms, "Administrative Debris". I interpreted "debris" as that which increases this conceptual distance I keep harping on. Her post, unlike mine, provides a lot more visual examples to get the point across. I would highly recommend reading her article to get another angle on these ideas.