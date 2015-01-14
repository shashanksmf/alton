# README #
**Name:** featured-scroll.js

**Version:** 1.0

**Author:** Paper Leaf

**Author Website:** http://www.paper-leaf.com

**Description:** A full featured scrolling plugin for creating immersive featured sections or headers.

**Copyright 2014 Paper Leaf Design**

## Quick start ##
### Featured Scroll. ###
The Idea behind featured scroll is that you have a header and footer section with a featured area of projects or something in the middle.

Here is an example for all the options available for featuredScroll:

First ensure you have the proper HTML structure:

```
#!html

<header class="header"></header>
<section class="full">
	<div class="slide"></div>
	<div class="slide"></div>
	<div class="slide"></div>
</section>
<footer class="footer"></footer>
```
Next add the following where you want to call it. Note: **If you don't want errors to occur, only run the script on the page where scrolling occurs**
```
#!javascript

$(document).scrollJack({
	fullSlideClass: 'full',
	firstClass: 'header',
	lastClass: 'footer',
	useSlideNumbers: true,
});
```

### Header Scroll ###
The Idea behind header scroll is that you have a featured header area, that on scroll disappears, an you find yourself at the main content, with native scrolling enabled.

Here is an example for all the options available for headerScroll:

First ensure you have the proper HTML structure:

```
#!html

<section class="header">
<!-- Insert Header Content Here -->
</section>
<section class="pageWrapper">
<!-- Insert Regular Content Here -->
</section>
```
Next add the following where you want to call it. Note: **If you don't want errors to occur, only run the script on the page where scrolling occurs**

```
#!javascript

$(document).scrollJack({
    firstClass : 'header', // classname of the first element in your page content
    bodyContainer: 'pageWrapper', // ID of content container
    scrollMode: 'headerScroll', // Choose scroll mode
});
```

## What's included ##

## Bugs and feature requests ##

Have a bug or a feature request? Please first read the issue guidelines and search for existing and closed issues. If your problem or idea is not addressed yet, please open a new issue.

## Documentation ##

## Keep track of development and community news. ##

Follow @twbootstrap on Twitter.
Read and subscribe to The Official Bootstrap Blog.
Chat with fellow Bootstrappers in IRC. On the irc.freenode.net server, in the ##bootstrap channel.
Implementation help may be found at Stack Overflow (tagged twitter-bootstrap-3).
Versioning

For transparency into our release cycle and in striving to maintain backward compatibility, Bootstrap is maintained under the Semantic Versioning guidelines. Sometimes we screw up, but we'll adhere to those rules whenever possible.

Creators

Mark Otto

https://twitter.com/mdo
https://github.com/mdo
Jacob Thornton

https://twitter.com/fat
https://github.com/fat
Copyright and license

## Code and documentation ## 
copyright 2011-2015 Twitter, Inc. Code released under the MIT license. Docs released under Creative Commons.


## Use Cases ##
There is a couple of features that this plugin covers.

To start things off here's every option that is available and it's default

```
#!javascript
$(document).scrollJack({
    firstClass : 'header', // classname of the first element in your page content
    fullSlideClass : 'full', // full page elements container for 
    nextElement : 'div', // set the first element in the first page series.
    previousClass : null, // null when starting at the top. Will be updated based on current postion
    lastClass: 'footer', // last block to scroll to
    slideNumbersContainer: 'slide-numbers', // ID of Slide Numbers
    bodyContainer: 'pageWrapper', // ID of content container
    scrollMode: 'featuredScroll', // Choose scroll mode
    useSlideNumbers: false, // Enable or disable slider pagination
    slideNumbersBorderColor: '#fff', // Choose pagination bullets border color
    slideNumbersColor: '#f8f8f8', // Choose pagination bullets fill color
});
```



## Frequently Asked Questions ##
#### Does this work on touchscreens? ####
No
#### Why not? ####
Touch events are a different beast, and considering the amount of people on cheaper, less powerful devices, or even the majority still stuck in contracts, the usability is usually non-existent. That being said, we are continuing to explore ways of implementing this for mobile devices.
#### So you are looking at adding mobile functionality? ####
Possibly
#### Scrolling appears unresponsive at times. What's going on? ####
After every scroll there's a delay in effect to help get rid of Inertia Scroll on Macs. If you try to scroll within this delay it will prevent you from scrolling, until the barrage of mousewheel events has ended.

## Possibilities for the next versions ##
* Custom Animations
* More Customization for slide number indicators (pagination)