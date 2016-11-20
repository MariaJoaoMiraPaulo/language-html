# Assignment 3

<a name="index"/>
## Index
1. [Introduction](#introduction)
2. [Logical View](#logical_view)
3. [Development View](#development_view)
4. [Deployment View](#deployment_view)
5. [Process View](#process_view)

<a name="introduction"/>
## Introduction

What is Software Architecture?

Microsoft answer:

>Software application architecture is the process of defining a structured solution that meets all of the technical and operational requirements, while optimizing common quality attributes such as performance, security, and manageability. It involves a series of decisions based on a wide range of factors, and each of these decisions can have considerable impact on the quality, performance, maintainability, and overall success of the application.

<a name="logical_view"/>
## Logical View

<a name="development_view"/>
## Development View

The Development view, also know as Implementation view is responsible for showing the project on development prespective. That view focuses on decomposing software into components. The component diagram's main purpose is to show the structural relationships between the components of a system.
This image shows the diferent components and the relationship between them.

![Image](https://github.com/MariaJoaoMiraPaulo/language-html/blob/master/ESOF%20-%20docs/res/atomComponentDiagram.png)

The overall architecture of Atom is organized around AtomEnvironment. The AtomEnvironment is the class responsible for dealing with packages, themes, menus, and the window.


<a name="deployment_view"/>
## Deployment View
The deployment view shows hardware nodes, communication relationships and software artifacts deployed on them.
On atom, not much happens. Only if you want to install a new package, or update a package that you already have installed.

![Image](https://github.com/MariaJoaoMiraPaulo/language-html/blob/master/ESOF%20-%20docs/res/atomDeployment.png?raw=true)

<a name="process_view"/>
## Process View
