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

#### Installing Sproutcore

Although developing a Sproutcore app requires Javascript skills exclusively,
the Sproutcore build and development helpers are written in Ruby and are
packaged in a RubyGem which also contains the latest stable version of the
Sproutcore Javascript library.

Therefore, this is how to install Sproutcore:

    $ sudo gem install sproutcore
   
(In this and subsequent examples, the `$` indicates a command prompt.) This
command will also install a number of Sproutcore's dependent RubyGems (aka
"gems"). At the moment, the Sproutcore tools work most fastest with the latest
version of Ruby 1.9, although they also work with Ruby 1.8.6 and 1.8.7. To
find the version of Ruby installed on your system, type:

    $ ruby --version
    
Instructions for upgrading Ruby are not included here; however, see the tip
below about using RVM, the Ruby Version Manager.

We will see that there is an easy pattern for supplanting the gem-supplied
version of the Sproutcore Javascript library in your individual projects,
making it unnecessary to update the gem to track updates to the Javascript
library. However, updates to the build tools are occasionally released. When
they are, you can install them by updating the gem as follows:

    $ sudo gem update sproutcore


_Tip_: If you want to update Ruby without mucking around with the system Ruby,
and/or prefer to maintain independent sets of gems for different purposes, you
may want to consider using RVM, the [Ruby Version Manager](http://rvm.beginrescueend.com/, "RVM").
If you were to install RVM (see the directions on the RVM website), you could
install Ruby 1.9.2 without overwriting your system Ruby as follows:

    $ rvm --install 1.9.2
    
Once you have installed the Ruby version you want, you can create a so-called
"gemset" that contains just the gems required for Sproutcore:

    $ rvm use 1.9.2                  # use Ruby version 1.9.2 in this process
    $ rvm gemset create sproutcore   # create a fresh gemset called 'sproutcore'
    $ rvm use 1.9.2@sproutcore       # use gems from/install gems to the new gemset
    $ gem install sproutcore         # install sproutcore and dependent gems to new gemset

Note that `sudo` is not required to install gems to a gemset.


#### What is included in the Sproutcore Gem

The Sproutcore gem includes two major components: the build and development
tools, and the Sproutcore Javascript itself. Supposing that gems are installed
into the directory `$GEM_HOME` and the current Sproutcore version is 1.4.1,
the build tools are copied into `$GEM_HOME/bin`, and the Javascript library is
rooted at `$GEM_HOME/gems/sproutcore-1.4.1/lib/frameworks/sproutcore`.

The Javascript library is the subject of most of the rest of this book. Don't
worry about the obscure location; it is easy to install an updated version of
the Sproutcore Javascript library into a more-accessible location inside your
project.

Here is a quick overview of the command-line build tools:

* `sc-build`: This follows the dependencies you declare between the Javascript
files in your application and outputs the compressed HTML, Javascript, and CSS
files that comprise your application. These are put into a directory whose
name is an MD5 hash that uniquely identifies one distinct build of your
application. You deploy your application by copying the files produced by
`sc-build` to a static web server.

* `sc-server`: This web server serves your application during development. It
watches for changes in your project directory as you develop, allowing you to
make changes to your Javascript on the fly and observe the resulting changes
by hitting the reload button in your browser.

* `sc-init`: This 'generator' initializes a new Sproutcore project directory.

* `sc-gen`: This 'generator' allows you to generate the appropriate
boilerplate code for several kinds of Sproutcore object with a single command.

* `sc-docs`: This documentation builder scans your application folder for
jsdoc-formatted comments and outputs a browseable HTML representation of your
applications' API, together with HTML-formatted source code. It is the tool
used to generate [http://docs.sproutcore.com](http://docs.sproutcore.com/).

#### Testing your Installation By Creating and Running the Welcome App
q
`cd` to your favorite development directory and run the command:

    $ sc-init examples
    
You can choose whatever directory name you like for the argument to `sc-init`.

The command should run and produce output similar to the following:

     ~ Created directory at examples
     ~ Created file at examples/Buildfile
     ~ Created file at examples/README
     ~ Created directory at apps
     ~ Created directory at apps/examples
     ~ Created file at apps/examples/core.js
     ~ Created file at apps/examples/main.js
     ~ Created directory at apps/examples/resources
     ~ Created file at apps/examples/resources/loading.rhtml
     ~ Created file at apps/examples/resources/main_page.js
    Your new SproutCore project is ready!

    To get started, you can find your initial application in the "apps" directory.

As you may be able to guess from the output, the `sc-init` generator creates a
Sproutcore "project" directory at `examples` (or whatever project name you
chose in the argument to `sc-init`) and filled it with some boilerplate
content. This content includes a complete, simple Sproutcore app, which at the
moment is also called `examples`.

A single project directory can contain multiple applications. Each folder in
the `apps` directory represents a different application. Applications in the
same project share a Buildfile (which customizes how `sc-build` and
`sc-server` construct the built application) and a `frameworks` directory (not
yet shown) where you can store common Javascript code shared between the
applications in a project.

You can run the simple application created by `sc-init`. Change to the
examples folder and run `sc-server` as follows:

    $ cd examples
    $ sc-server -v

The `-v` option specifies verbose operation, in which `sc-server` logs to the
terminal window which file it is serving as it serves it. This is helpful for
understanding what `sc-server` is doing.

Now, open [http://localhost:4020/](http://localhost:4020/) in a web browser.
There is likely to be a pause as `sc-server` thinks (it is spidering the
Sproutcore source and the applications in your project folder, and caching the
results into a newly-created `tmp` directory in the root of your project for
speedier loading on subsequent reloads).

After a few moments, you should see a "Sproutcore Developer Tools" control
open up in the center of the page, presenting a choice of several applications
to load, with a "Load Application" button below.

Choose the 'examples' application and click "Load Application". You should see
a screen with the text:

    Welcome to SproutCore!
      
displayed in the center of the page. If so, congratulations! Your Sproutcore
installation is ready to use.


#### Aside: Development on Windows


#### Aside: Setting up TextMate

* The most common development environment is TextMate
* You can install a very helpful "Sproutcore bundle"
* tip: once you start an app, open the app folder not the


#### Tutorial: A test-driven Hello, World

#### Javascript Resources


Sproutcore Basics 
-----------------

### Sproutcore's Custom Class and Object System

#### How to "Read" the Hello Application

#### Introducing `SC.Object`

#### Mixins, `init()`, `initMixin()`, and `sc_super()`


### Tying an Application Together Using Key Value Coding, Key Value Observing, and Bindings

### Tutorial Break: Making a Slick, Touch-enabled App


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
