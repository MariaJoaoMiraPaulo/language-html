# Project 2

<a name="index"/>
## Index
1. [Requirements Elicitation](#requirements_elicitation)
2. [Specific Requirements and Features] (#specific_requirements)
3. [Use Cases](#use_cases)
4. [Domain Model](#domain_model)
5. [Contributions](#group_contribution)

<a name="requirements_elicitation"/>
## Requirements Elicitation

We asked Lee Dohm (Atom Community Manager), on Slack, how does his team decide which features to implement next:

Lee's answer:

> We have been experimenting with various ways of figuring out what to tackle first. With over 4,000 issues across all 190+ public Atom repositories, there's a *lot* to choose from :grinning: Our current system is that we address regressions first, things that are broken now but did work at one time. At roughly the same level of priority are build failures. After that we have bugs and feature work. Some feature work involves large parts of or the whole team, other features are done on an individual basis. The individual stuff is generally done to get a break from the stuff we _have_ to work on so it's pretty much left up to the individual's discretion, though we influence each other a lot. The large features are generally things that we want to add to Atom strategically and there is generally at least one of these going on at any time. Whether non-regression bugs come before feature work or vice versa is roughly determined in negotiations between the Engineering Manager and myself. The edge is generally given to bugs.


We also asked him what's their process to accept Pull Resquests, which he answered:

> The process for getting a Pull Request accepted is that the triage team, mostly made up of our awesome volunteer maintainers, takes a look at it first, ensuring it has the minimum needed to get another maintainer to take a look. Our volunteer maintainers though often have their own areas of expertise, so if the person doing the triage can judge it by themselves, they do. Once the triage maintainer thinks it is ready for review, they label it `needs-review` and eventually the maintainer who owns that package reviews it and works with the author to get it merged.

>There are a lot of other things that go into getting a Pull Request accepted and it is often one of the more challenging and time consuming things we do. One of the reasons for the new triage process is to try to help people know what they need to provide us with so that they can get their PR accepted without a lot of back-and-forth.

He also said that Atom's working on a new PR triage process:

>I'm actually working on a new Issue and PR triage process that we'll be rolling out soon with a detailed blog post explaining why the new process is the way it is





<a name="specific_requirements"/>
## Specific Requirements and Features

Functional Requirements

When Atom is starting, it gathers all the packages installed by the user and puts them ready for use anytime the user selects them.

Once loaded, the user can add, create or open a file. Upon the selection of one of these, the system has to instantly open a new tab with the file content while showing the directory path on the left of the screen. If the user desires, the system shall allow him to open more files at the same time and respectively generating new tabs, adressing to the files content.

At this stage, the system will allow the user to write or delete any text existing on the file aswell as saving the file as it is and closing it aftewards.

Functional requirements vary due to the packages installed and selected while running Atom, so, here are only the main requirements without extra packages.


Non Functional Requirements


The project should be developed mainly in CoffeScript and/or JavaScript.

It shall remain free of cost and reachable to anyone who wishes to use it.

Atom shall maintain its package system in order to maintain the light start of the program and enable the open source community to help on the developing process.


<a name="use_cases"/>
## Use Cases

As far as use cases go we asked Lee Dohm if their team analises use cases, in order to decide what to develop next, which he said:

>we do look at use cases for _how_ to design things, but we don't really use them as a way to determine prioritization, no

![Image](https://github.com/MariaJoaoMiraPaulo/language-html/blob/master/ESOF%20-%20docs/res/useCases.jpg?raw=true)





<a name="domain_model"/>
## Domain Model

![Image](https://raw.githubusercontent.com/MariaJoaoMiraPaulo/language-html/master/ESOF%20-%20docs/res/domainModel.png)




<a name="group_contribution"/>
## Contributions

  Maria João Mira Paulo : 25%;

  Nuno Ramos : 25%;

  Pedro Costa : 25%;

  Ricardo Neves : 25%;
