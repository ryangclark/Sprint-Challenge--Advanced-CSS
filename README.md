# Sprint Challenge: Advanced CSS - Space Walkers Web Page

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a concrete project. This Sprint explored advanced CSS techniques using Responsive Design and Preprocessing. During this Sprint, you studied how to use the viewport meta tag, media queries, setting up a preprocessor, and advanced use of preprocessing techniques. In your challenge this week, you will demonstrate proficiency by updating a website that is missing content as well as adding mobile styling.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in advanced css and your command of the concepts and techniques in responsive web design and preprocessing.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your project manager.

## Description

The client for this challenge is _Spacewalkers Magazine_. Spacewalkers needs your help to build a small proof of concept website for their marketing team. They have provided designs for both desktop and phone views. In addition to designs and content they have most of the home page coded for you. You just need to finish the navigation and header as well as the mobile styles.

In meeting the minimum viable product (MVP) specifications listed below, your web page should look like the solution design files of the desktop and mobile views:

[Click here to review the home design](design-files/home-desktop.png)

[Click here to review the mobile design](design-files/home-mobile.png)

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager

1. What is the difference between an adaptive website and a fully responsive website?

An "adaptive" website is best defined in contrast to a "fixed" website. A fixed site is one with elements that are sized rigidly, with set measurements that do not take into account the size of the user's screen. An adaptive one, however, uses sizing mechanisms (such as percentages) that allow for some adaptation of element sizes while maintaining the overall layout. 

A "fully responsive" website is one with elements that are not only adaptive, but a layout that also changes in response to different screen sizes. For instance, when shifting from a desktop resolution to a phone resolution, the navigation menu items will not simply get smaller but might change their position and layout, or even hide themselves into a hamburger menu that the user can toggle when needed.

2. Describe what it means to be mobile first vs desktop first.

The above terms refer to both design and developement mindsets – the team creates either the mobile interface or the desktop interface first, and adapts the other from that. In my experience, designing mobile interfaces first is the smarter policy for the long-term because it can often be difficult to make an engaging *and* simple interface, especially when including relatively complex features, for a small screen. Doing so requires ingenuity in building intuitive menus, properly spacing elements for "fat fingers", utilizing gestures, and much more. Do the hard thing first. Then, expanding that interface to a larger screen is relatively trivial – you have so much more room to play with now, so it's not too hard to preserve the engaging and intuitive characteristics of your interface.

If, however, you go from desktop to mobile, things can be hard. You're trying to adapt an interface with plenty of space to one that is much more restricted. All of a sudden your spacious menus and expansive data tables don't fit. What do you do? Typically, you'll end up designing something new instead of simply adapting the desktop. You've done twice the work.

Think of it this way: Instagram was a mobile-first app, and Facebook is a desktop-first site. Open Instagram on your desktop, and the interface feels quite similar to the mobile one. It's just a bit bigger, but everything is in the same place and works the same way. Now, take Facebook. Their mobile app feels quite different from the desktop site because they had to create new interfaces for the smaller screen. One isn't necessarily better than the other – perhaps experiences *should* feel different on different devices – but one is definitely twice the work.

In terms of development (which is probably what the question is actually about), similar principles apply. In mobile-first, you begin by creating styles and elements for the smallest screens first, and use CSS media queries to expand that original interface at your breakpoints. The cascade begins small, and expands up. The opposite is true of desktop-first: you create styles and elements for the largest screen first, and adapt those with CSS for each progressively smaller breakpoint.

3. What does `font-size: 62.5%` in the `html` tag do for us when using `rem` units?

Typically, users use their browser's default font-size, which is 16px. And 62.5% of 16 is 10, which is a much more convenient number for developers to use. By taking the user's font size setting as an input and referring to it throughout the site by using `rem`, the site is more accessible to users who change that setting. It responds to their needs without requiring them to hit `cmd +` every time they open a new webpage.

4. How would you describe preprocessing to someone new to CSS?

CSS is pretty straightforward. It has specific rules, and a strict cascade. That's nice, and it allows developers to create beautiful websites. But CSS doesn't have powerful tools and features, which are common to other programming languages, that would make using CSS much more efficient and smart.

Since browsers won't change how they read CSS, developers instead decided to create a better version of CSS. What they figured out is that they could write CSS with those abstractions and variables and the other features they wanted, then have a program translate that code into browser-level CSS. It's like hiring a general contractor to redo your kitchen: you tell the general contractor the type of cabinets and countertops you want, then she explains the specifics to the plumber, the painter, the cabinet folks, etc. You get the kitchen you want without having to worry about every detail.

5. What is your favorite concept in preprocessing? What is the concept that gives you the most trouble?

I quite like mixins and variables. I can see how they would be very valuable in making changes to a site quickly and easily – rather than having to track down every single `(max-width: 500px)` throughout your thousands of lines of CSS, you can just change a variable or two and have the preprocessor do the heavy lifting.

The hardest thing is related: how do you structure your code to take advantage of those variables and mixins? Creating that chained structure of variables takes time, effort, and skill upfront. You have to think ahead to plan "What are all the things that I might want to change? And how do I make that easy to do?" Tricky at best.

You are expected to be able to answer all these questions. Your responses contribute to your Sprint Challenge grade. Skipping this section *will* prevent you from passing this challenge.

## Project Set Up

Because you are using a preprocessor, there are two parts to setting up your project.  Be sure to run through the git set up first and then set up the preprocessor.

### Git Set up

Follow these steps to set up your project:

- [x] Create a forked copy of this project.
- [x] Add your project manager as collaborator on Github.
- [x] Clone your OWN version of the repository (Not Lambda's by mistake!).
- [x] Create a new branch: git checkout -b `<firstName-lastName>`.
- [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
- [ ] Push commits: git push origin `<firstName-lastName>`.
 
Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo). **Please don't merge your own pull request**
- [ ] Add your project manager as a reviewer on the pull-request
- [ ] Your project manager will count the project as complete by merging the branch back into master.
 

### Preprocessor Set up

* [x] Verify that you have LESS installed correctly by running `lessc -v` in your terminal, if you don't get a version message back, reach out to your project manager for help.
* [x] Open your terminal and navigate to your preprocessing project by using the `cd` command
* [x] Once in your project's root folder, run the following command `less-watch-compiler less css index.less`
* [x] Verify your compiler is working correctly by changing the `background-color` on the `html` selector to `red` in your `index.less` file.
* [x] Once you see the red screen, you can delete that style and you're ready to start on the next task

## Minimum Viable Product

Your finished project must include all of the following requirements:

### Import LESS Files

* [x] Navigate to your `index.less` file. Notice the file is blank. You have been asked to use a certain import order. That order is as follows:

```markdown
1.variables.less
2.mixins.less
3.reset.less
4.global.less
5.navigation.less
6.footer.less
7.home-page.less
```

_You will know everything is working properly when you see the styles enabled for the provided content._

### Home Page - Desktop HTML & LESS

* [x] Take 10 minutes to review the code that has already been provided for you. Take time to see how the home page was built.

* [x] Add a viewport meta tag to the head of your index.html page

* [x] [Review the provided home desktop design file](design-files/home-desktop.png). You are to build the missing navigation system and header image. You have been provided all content necessary in the [index.html file](index.html)

* [x] Navigation Styles: Use the `navigation.less` file for styling.

* [x] Main Content Styles: Use the `home-page.less` file for styling

* [x] LESS Mixins: Create and use 2 different mixins to aid your styling. Use the `mixins.less` file for your mixins

* [x] LESS Parametric Mixin: create a parametric mixin that is used to create the `sign up` button styles.

* [x]  Use at least 2 parameters to create your button

* [x] Create a hover state that swaps the background color and font color of the base button styles.

### Mobile Design

* [ ] Create a `@phone` variable that contains a `max-width: 500px` media query string. Use the `@phone` variable for all your nested mobile styling.

* [ ] [Review the provided home mobile design file](design-files/home-mobile.png). Match your mobile styling the best you can using the design file.

* [ ] Push your changes and create a pull request if you haven't already.

In your solution, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

After finishing your required elements, you can push your work further. These goals may or may not be things you have learned in this module but they build on the material you just studied. Time allowing, stretch your limits and see if you can deliver on the following optional goals:

* [ ] Build a page of your choosing from the navigation items. Come up with content and images that fit the theme.

* [ ] Introduce CSS animations to your site.

* [ ] Create a fixed navigation and add some opacity to the background

* [ ] Create a form that would allow someone to sign up for a Spacewalkers Magazine subscription