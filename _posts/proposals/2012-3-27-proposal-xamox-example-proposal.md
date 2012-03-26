---
layout: post
category : proposals
tags : [proposals, proposal]
---
{% include JB/setup %}

This was one of the core simplecv developers Summer of Code 2007 submission.
It was for the open source project drupal.  It's expected your's will
be similiar but directed towards the projects listed on:
http://soc.simplecv.org


-----------------------------------

Name: Anthony Oliver

Alias: xamox

Project Title: Extend Case Tracker Module

Overview: Make case tracker more project management friendly.

Motivation:

The idea of this project is give Drupal the same type of functionality as Microsoft Project or Planner, by extending the Case Tracker module. Currently the cast tracker module is setup as more of a ticketing system for tracking projects but lacks the some of the features I think a project management system needs. The extension I'm proposing would allow for a visual representation of the project, and track resources as a drop in replacement to give an “out of the box” solution for Drupal. The case tracker also doesn't give a way to track cost of resources used within a project nor does it give the ability to do projections of where a project is overall and how long a project would take visually. Currently the way the module works is a case is created (a task) and is assigned to a user. The user then has the ability to perform the task and leave feedback if it was taken care of or not and change the state of the case. With the extension I'm proposing the project manager could estimate the time it would take for the project to be complete and analyze what resources are available, and assign task accordingly. It would also give the ability to review how much time projects took and plan for future projects based on the previous ones.
I've seen the need within the 2 software companies I have worked for. One was in the field of vision guided robotics and the other roadway asset management software. Both are software companies, but need something outside the functionality of versioning and ticketing software from the standpoint of management. For instance for the vision guided robotics company each job (project) we took, everything was kept on paper, no one knew who did what to the system, what status the project was in, which ended up in calling a lot of people on the phone, and wasting a lot of time, as well as no idea how much actual time was spent per project. The second programming company is state funded, which means yearly proposals to get funding for the next year. So the proposals require that man hours be projected and how much funding will be needed. So this module would serve two purposes, the first being it allows a generalized interface (web based) to track where resources are being used withing an organization; and secondly functions as a time logger and a way to project cost, time, and resources for future projects.

Deliverables:

Visual representation (Gannt chart) will be provided to give an overall view of cases (task) within a project.
Use jQuery to control visual Gannt chart and change length of time for various cases (tasks).
Add the ability to edit an event date (event attached to a case) without editing node permissions.
The ability to stall (or extend) a project if it doesn't meet the deadline.
Use CCK user reference to control resources and assign various cases amongst users (will replace existing assign to method).
Add User Interface enhancements as Dries suggest here: http://drupal.org/node/104467, that include: making things such as priorities more intuitive, and case's listed under projects instead of on separate pages (sub-task via indentation).

Remarks:

I have been discussing this project extension with Morbus (creator of the case tracker module) and has offered to give me guidance if need be. Also discussed a little bit with sime (emspace on IRC) about features. I have also discussed this idea with various people within the Drupal support IRC channel and a lot of people said they could see it as a useful module. I talked to kkaefer as well on IRC and he mentioned I should note why I would like to use jQuery. I would use jQuery for one, because it is part of the Drupal 5 core now, and secondly after spending time looking at the library's website I believe it can do what I want it to for this project. There is also a lot of resources for jQuery such as http://www.visualjquery.com that make learning syntax and the API, as well as a jquery IRC support channel, and modules in Drupal that currently use jQuery that I could use as examples. Which should make jQuery integration acceptable within this projects scope and timeline.
I think this project is something that would help Drupal become more of a community management system in addition to being a content management system. I also believe this could offer Drupal another advantage by offering competition to various service oriented architecture (SOA) based websites, such as devshop and basecamp. Although I don't expect to have the same feature set offered by the fore mentioned websites, what this module would offer is a free alternative that would integrate within an organizations Drupal based website.

Timeline:

April 10 to May 27:
* get CVS account
* start talking to mentors about development plan and needed routes
* get in touch with Dries about user interface design he would like to see as mentioned on http://drupal.org/node/104467 and draft a mockup.
* Talk to Morbus about design and database schema he recommends for the project
* start going through http://drupal.org/contributors-guide and looking at keeping code secure, methods for submitting, test cases, etc.
* Start tearing apart various modules to see how they actually work (especially ones that currently use jQuery).
* Write some basic jQuery examples in a simple mock up module.

May 28 to June 15:
* Try get a basic Gannt Chart built using jQuery
* Get a basic alpha version of module going
* Keep tight contact with mentor(s) and make sure heading right direction
* Get code reviews from mentors

June 15 to July 9:
* Get beta version of module extension working and submit to Google for midterm review

July 16 to August 20:
* Make changes according to midterm review.
* Polish up and any code and make design changes if needed, have mentors & peers review code for security/bug fixes
* Find some beta testers for the project and get feedback and make adjustments.
* Submit module extension for final evaluation to Google.

August 31:
* Announce module to Drupal Community

Future:

This module could eventually offer all the features that sites like SOA websites like basecamp and devshop, or programs like Microsoft project. Eventually form input could all be AJAX driven possibly through integration with AHAH Forms module

About Me:

I am currently obtaining my degree in Software Engineering from Michigan Technological University (one semester left). I have been involved with programming since about the age of 14 when I got a home certification in PC Repair. I am a heavy user of open source software (all software, including operating system is open source). I have been the president of the local Association for Computing Machinery (ACM) chapter, as well as a part of the local Linux user's group (LUG). I have worked as a Summer Youth Teacher at Michigan Tech teaching Java and C++ to younger students, as well as a Computer Science Learning Center Coach. As a Senior Design project I worked in conjunction with the Navy on a project dubbed, Seabase, in which we used MATLAB to stabilize a payload on a sea crane. Worked for Professor Dr. Charles Wallace at Michigan Tech helping develop a XML case study tool for Software Quality Assurance. Worked within the Robotics Enterprise at Michigan Tech as well as doing embedded programming for hardware/software integration. I have worked for a Vision Guided Robotics company doing software development in Visual BASIC 6/.NET as well as routine IT person for them at the Houghton Innovation Center Office in Houghton, MI. I am now currently working for a Roadway Asset Management Software company that makes the software the Michigan Department of Transportation uses and finishing up getting my degree.

I have been involved with Drupal for about 8 months now. I am very active within the Drupal support channel on IRC as well as submitting bug reports for Drupal. Recently I have been getting more involved within the community by testing new modules, staying up with the Drupal dojo, listening to the lullabot podcast, and have been considering writing a module for a while now. I am in the process of starting my own consulting business, which of course would be using Drupal as the platform for web development so you can expect me to stay active within the Drupal community. On Dries learning curve chart (http://buytaert.net/drupal-learning-curve) I am about at the theme and module development section. To show my initiative I have started learning how to write a basic module on my own time and trying to learn the basics of jQuery and have created a Drupal install at http://xamox.net/drupal/ specifically for this. I also just pre-ordered the Pro Drupal development book that comes out April 9th and believe this would be a good supplement/resource for the summer of code project. Taken into consideration my activity within the Drupal community over the past 8 months, as well as my Software Engineering background, I believe I am a strong candidate to be a summer of code student, if not for this project any other.
