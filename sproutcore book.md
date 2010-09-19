The Sproutcore Book 
===================

Introduction 
------------

### About This Book

This book aims to become a comprehensive introduction to Sproutcore, an open
source framework for building apps with HTML and Javascript. Sproutcore is
well-designed, comprehensive, and highly tuned as a result of early adoption
by Apple as the foundation of the Mobile Me and iWork.com services. Yet the
combination of Sproutcore's comprehensive scope and its adoption as a
non-revenue-generating product by a secretive company have worked against it.
Only the most motivated or stubborn non-Apple developers have had cause to
read through its source code and its sometimes sparse documentation enough to
learn how to use it to build professional-class applications.

Fortunately, with the help of the approachable and growing community of
Sproutcore developers--a community which exists because of maintainer Charles
Jolley's determination to keep his project genuinely open--the situation is
rapidly improving. This book is one of several efforts that are being made to
help mainstream developers use Sproutcore to write apps that are as fast,
fluid, and flexible as any native app--yet that can be run in nearly any web
browser merely by clicking on a link.

This book has three sections. The Introduction explores briefly what it means
to say that Sproutcore helps you write web apps, and describes the
technological features of Sproutcore that help you to do so. Because you
should be eager to get busy at this point, the second chapter describes how to
install Sproutcore, describes what you see when you install it, and points you
to several hands-on tutorials.

The second section, "Sproutcore Basics", is a tour of the individual
components of Sproutcore that every Sproutcore developer should be familiar
with. After having read it, you should be able to construct a basic app with
little fear that you are ignoring large parts of Sproutcore. Important
"gotchas" and tips are highlighted, where necessary with links to reference
documents or the more detailed third section, in order to provide context.

Finally, the third section, "Sproutcore in Detail", revisits most of the
components discussed in "Sproutcore Basics" at a more reference-like level of
detail, though still in narrative fashion. After reading this section, you
should be well equipped to dive into the Sproutcore reference documentation
and source code without feeling lost.

Some words of warning before you proceed: Sproutcore requires a very different
mindset than traditional front-end web development. It is not a tool for
writing progressively enhanced web documents but is for writing *apps* that
run atop what one might call "the HTML and Javascript platform". To use it
well requires mastering a large number of libraries and tools that work
together and cannot be learned overnight. More profoundly, Sproutcore may
require you to unlearn some web development habits. Because download and
browser rendering times have decreased dramatically but the time required for
round-trips to servers has not, Sproutcore uses Javascript to render your
app's screens from client-side data. It also encourages you to move most of
your app's logic to the client. If you write web applications this may seem
wrong. This book is here to keep these instincts from getting in your way as
you learn to work with the grain of Sproutcore.


### What is Sproutcore?

#### What Sproutcore Does For You

Sproutcore is a well-engineered open source framework for making web apps.
However, Sproutcore apps are unlike Ajax web applications and have more in
common with the apps of the "App Revolution" the mobile world has undergone in
the last few years. Apps for our phones and tablets are often faster, more
fluid, and more focused than Ajax web pages. Sproutcore helps you make
similarly fast and fluid apps--except that you run them by visiting an
ordinary web page in an ordinary web browser.

This means that Sproutcore should not be confused with a tool for making web
documents; for that job you want semantic HTML progressively enhanced with
carefully chosen Javascript. But in the years since it became dogma to *only*
use such technology, the terms of engagement have changed. Broadband pipes
have become bigger; browsers have gotten faster and much more sophisticated;
and users have come to expect and understand app-like experiences.

A few years ago, Apple foresaw these changes and adopted Sproutcore for
building Mobile Me and iWork.com. In the process Sproutcore received an
enormous endowment of engineering effort and fine-tuning that you can now put
to work for yourself. Using Sproutcore, you can deploy one app to all your
users, whether at any moment they happen to be using Internet Explorer on a
locked-down PC at work, the Android phone in their pocket, or the iPad on a
friend's coffee table.

Moreover, because Sproutcore is open-source and based on HTML and Javascript,
you can be sure that your app will work on new devices--even new classes of
device, like multitouch tables and interactive whiteboards--for years to come.

Best of all, Sproutcore comes with a friendly, active, and growing community that will help you to make your app the best it can be.


#### How Sproutcore Does It

Sproutcore achieves app-like responsiveness in ordinary browsers not by magic
but by recognizing a new balance among technological factors: download
throughputs and browser speeds are continually decreasing while round-trip
times to servers are decreasing much more slowly. Therefore it is now often
better to take a few extra milliseconds to download a fat javascript package
that knows how to render and navigate among multiple screens than it is to
incur the lag involved in asking the server to render a new HTML page every
time the user navigates; and it can be better to pre-fetch a large amount of
server-side data to your client in the background than it is to round-trip to
the server every time the user touches data.

Sproutcore includes abstractions that help you write Javascript that works
with the grain of these new realities. Moreover it includes libraries and a
Javascript-friendly object system that help you program "in the large"; build
tools that help you divide up your Javascript into manageable pieces; a unit
testing framework; and deployment tools that transparently optimize the
chances that clients will use a cached version of your app's code.

...

Sproutcore doesn't try to be magic; it's just a large Javascript library and a well-thought out build system that supply the missing pieces you will find yourself wanting if you try to build a slick, fast app "from scratch" using only HTML, Javascript, and libraries like jQuery and jQueryUI. 


### Installing Sproutcore, Finding the Tutorials, and Setting Up a Development Environment


Sproutcore Basics 
-----------------

### Sproutcore's Custom Class and Object System

### How the Build Tools, Development Server, and Your Browser Turn Your Project Files into a Running Application

### Tying an Application Together Using Key Value Coding, Key Value Observing, and Bindings

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
