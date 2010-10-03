The Sproutcore Book 
===================

Introduction 
------------

### About This Document

This book aims to become a standard introduction to Sproutcore, an open source
framework for building native-style apps with HTML and Javascript. Sproutcore
is comprehensive, well-designed, and highly tuned as a result of its early
adoption by Apple for powering the Mobile Me and iWork.com web apps. Yet
Sproutcore's massive scope and its history of development at a secretive
company have worked against it. Until recently only the most motivated and
stubborn non-Apple developers have had cause to study its voluminous source
code and comparatively sparse documentation well enough to truly learn it.

Fortunately, with the help of the approachable and growing community of
Sproutcore developers--a community which exists because of maintainer Charles
Jolley's determination to keep his project genuinely open--the situation is
rapidly improving. This book is one of several efforts to help mainstream
developers learn to use Sproutcore to write apps that are as fast, fluid, and
flexible as any native app, yet that can be accessed in nearly any web browser
merely by clicking on a link.

This book has three sections. This section, the Introduction, explores briefly
what it means to say that Sproutcore helps you write native-style web apps,
and describes the technological features of Sproutcore that help you to do so.
Since you will probably be eager to get your hands dirty at that point, the
second chapter of the Introduction describes how to install Sproutcore and
describes the components of the installation. It includes a tutorial that
shows you how to write, test, and deploy a "hello, world" application that
implements some some basic behavior.

The second section, "Sproutcore Basics", is a tour of the individual
components of Sproutcore that every Sproutcore developer should be familiar
with. After having read it, you should be able to build a straightforward app
with little trouble. Important "gotchas" and tips are highlighted and
annotated, where necessary, with links to reference documents or the more
detailed third section that provide more context.

Finally, the third section, "Sproutcore in Detail", revisits most of the
components discussed in "Sproutcore Basics" at a more reference-like level of
detail. After having read this section, you should be well equipped to dive
into the Sproutcore reference documentation and source code without feeling
lost.

Some words of warning before you proceed: Sproutcore requires a very different
mindset than traditional front-end web development. It is not a tool for
writing progressively enhanced web documents but is for writing *apps*,
distinct from your content, that treat HTML and Javascript as an execution
platform. To use it well requires mastering a large number of libraries and
tools that work together and cannot be learned overnight. More profoundly,
Sproutcore requires you to put aside certain web development habits.
Sproutcore's designers observed that download and browser rendering times are
decreasing at a steady rate while round-trip times to servers simply cannot,
and therefore designed Sproutcore to construct your apps's HTML on the client,
using Javascript. In general they provide tools that help you move as much
application logic to the client as possible. This may feel wrong at first.
This book is here to help you grasp the thinking behind these decisions and
thereby work with the grain of Sproutcore rather than against it.


### What is Sproutcore?

#### What Sproutcore Does For You

#### How Sproutcore Does It


### Getting Started

#### Installing the Sproutcore Gem

#### Setting up TextMate

#### Aside: Development on Windows

#### Tutorial: A test-driven Hello, World

#### Building the Hello Application for Deployment

#### Javascript Resources


Sproutcore Basics 
-----------------

### Sproutcore's Custom Class and Object System

#### How to "Read" the Hello Application

#### Introducing `SC.Object`

#### Mixins, `init()`, `initMixin()`, and `sc_super()`


### Tying an Application Together Using Key Value Coding, Key Value Observing, and Bindings


### How the Build Tools, Development Server, and Your Browser Turn Your Project Files into a Running Application


### Storing Your Data With Models, RecordArrays, and Fixtures


### Using Controllers to Manage Models and Views


### Using Views to Make Actual HTML


### Managing Views and Panes with Container Views and Page Objects


### Using Common View Classes To Solve Common Problems


### Using Collection Views To Display Collections of Objects


### Implementing a Data Source to Store Persistent Data


### The Architect's Toolkit: Routes, Pages, States, Application Events, and High Level Controllers


### Using QUnit and TestRunner to Unit Test Your Application


Sproutcore In Depth 
-------------------

### Classes, Objects, and Mixins


### The Build System and Application Deployment


### Setters and Getters, Observers, and Bindings


### Records, Queries, and RecordArrays


### The Data Store


### Data Sources


### Object Controllers


### Array Controllers


### The View Lifecycle and Rendering Path


### Writing Custom View Classes


### Collection Views


### Writing Custom Collection Views


### Event Handling


### Runloops


### ResponderContexts and the Responder Chain


### SC.routes


### CoreTest, TestRunner and Test Fixtures
