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
