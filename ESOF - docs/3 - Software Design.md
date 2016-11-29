# Assignment 3

<a name="index"/>
## Index
1. [Introduction](#introduction)
2. [Logical View](#logical_view)
3. [Development View](#development_view)
4. [Deployment View](#deployment_view)
5. [Process View](#process_view)
6. [Contributions](#group_contribution)

<a name="introduction"/>
## Introduction

What is Software Architecture?

Microsoft answer:

>Software application architecture is the process of defining a structured solution that meets all of the technical and operational requirements, while optimizing common quality attributes such as performance, security, and manageability. It involves a series of decisions based on a wide range of factors, and each of these decisions can have considerable impact on the quality, performance, maintainability, and overall success of the application.

To study atom software architecture we going to use the 4x+1 architectural view model. The 4+1 View Model describes software architecture using five concurrent views, each of which addresses a specific set of concerns:

  * The logical view - describes the design's object model, the process view describes the design's concurrency and synchronization aspects;

  * The deployment view - describes the mapping of the software onto the hardware and shows the system's distributed aspects;

  * The development view - describes the software's static organization in the development environment;

  * The Process view - deals with the dynamic aspects of the system, explains the system processes and how they communicate, and focuses on the runtime behavior of the system;

  * The use-case view - this view is the adtional view (+1), it describes the user´s interaction with the system that shows the relationship between the user and the different use cases in which the user is involved;

  ![Image](https://github.com/MariaJoaoMiraPaulo/language-html/blob/master/ESOF%20-%20docs/res/4+1.gif?raw=true)
  
What is the architectural pattern followed by Atom? 

The architectural pattern followed by Atom is Component-Based Architectural Style. Component-based architecture describes a software engineering approach to system design and development. It focuses on the decomposition of the design into individual functional or logical components that expose well-defined communication interfaces containing methods, events, and properties.   
Atom is divided in packages that decompose the whole software into smaller components(packages). Each package represents an individual and extra functionality. Atom's core and its independent packages compose Atom, offering a higher level of abstraction. This allows Atom to be scalable.

<a name="logical_view"/>
## Logical View
In the logical view we'll show the main classes that define the atom engine.

![Image](https://github.com/MariaJoaoMiraPaulo/language-html/blob/master/ESOF%20-%20docs/res/class-diagram.png)

The main class is AtomEnvironment, it is called in the beggining of the program and it calls all the other functionalaties. Some of the main functionalaties/classes are:
  * Config, this class holds and manages all Atom's configuration details;
  * PackageManager, it controls and loads all the installed packages, which one of the key elements of Atom's editor;
  * TextEditor, and all its TextBuffers, which contains the tools needed for writing and editing files as well as the undo/redo functionalaty;


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

![Image](https://github.com/MariaJoaoMiraPaulo/language-html/blob/master/ESOF%20-%20docs/res/AtomActivityDiagram.png?raw=true)


As it is shown in the activity diagram, the starting point is launching the application.
After doing it, we get to the users interface that allows us to choose from a certain range of options. We can manage the configurations, install packages or themes, use packages or themes (user selected), and control settings. As far as using the application for it's main purpose, it is given the choice to open a file or create a new one in the interface and after that, also in the interface, we can write or delete text and then save it.
With all of these activities we can only reach the end state in the interface before we open a file or after saving it.

<a name="group_contribution"/>
## Contributions

  Maria João Mira Paulo : 25%;

  Nuno Ramos : 25%;

  Pedro Costa : 25%;

  Ricardo Neves : 25%;
