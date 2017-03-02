# Mobile at Scale: Building a Lasting Architecture

* [Panel](#panel)
  * [Facebook Omega Logistics (Kasia)](#facebook-omega-logistics-kasia)
  * [Facebook Android App Reactions (Jenny)](#facebook-android-app-reactions-jenny)
  * [Intuit QuickBooks Self-Employed (Kristina)](#intuit-quickbooks-self-employed-kristina)
  * [Workflow iOS (Ayaka)](#workflow-ios-ayaka)
  * [Pinterest (Wendy)](#pinterest-wendy)
* [Q&A](#qa)
  * [How has your codebase changed as your team has gotten larger?](#how-has-your-codebase-changed-as-your-team-has-gotten-larger)
  * [How do you make an app work well for users in all parts of the world?](#how-do-you-make-an-app-work-well-for-users-in-all-parts-of-the-world)
  * [Things we can do to keep accessibility in mind?](#things-we-can-do-to-keep-accessibility-in-mind)
  * [Scalability of testing?](#scalability-of-testing)
  * [React Native for app extensions?](#react-native-for-app-extensions)
  * [Why did you use React versus other options?](#why-did-you-use-react-versus-other-options)
  * [How do you get into mobile architecture? Any tips?](#how-do-you-get-into-mobile-architecture--any-tips)
  * [What did you find were your most transferrable skills working across multiple apps?](#what-did-you-find-were-your-most-transferrable-skills-working-across-multiple-apps)
  * [How do you measure performance before release, or even before cutting the release build?](#how-do-you-measure-performance-before-release--or-even-before-cutting-the-release-build)

## Panel

**Moderator:** Wendy Lu (Pinterest iOS)  
**Panelists:** Kasia Hayden (Facebook), Ayaka Nonaka (Workflow iOS), Kirstina Thai (Intuit iOS), Jenny Yuen (Facebook Android)

### Facebook Omega Logistics (Kasia)

iOS vs Android?  
Building an app for Facebook data teams.

React Native

* Framework for building native apps using React, a JS library for building user interfaces
* Compiles to native code (Java or Obj-C)
* Extensible – incorporate native code easily

Walkthrough of the F8 2016 App, from Facebook's annual developer conference:  
[http://makeitopen.com/tutorials/building-the-f8-app/planning/](http://makeitopen.com/tutorials/building-the-f8-app/planning/)

Pain points?

* Higher-order functions
* Scope and context are different
* Hybrid app best practices: control branching for different platforms
* Navigation is tricky
  * mynavigationbar.ios.js  / mynavigationbar.android.js

### Facebook Android App Reactions (Jenny)

Building for delight: Animations  
Design team used After Effects: High fidelity animations

Scaling challenges

* Resizable
* High fidelity
* File size
* Performance: frame rate, load time

|               | Resizable | High Fidelity | Compact Size | Performance |
|---------------|:---------:|:-------------:|:------------:|:-----------:|
| **PNG**       | No        | No            | Yes          | ?           |
| **GIF**       | No        | No            | Yes          | ?           |
| **WebP/WebM** | No        | No            | Yes          | ?           |
| **SVG**       | Yes       | Yes           | No           | ?           |

Adobe ExtendScript

* After Effects file > extracts all visible information
* Key information:
  * Animation layers: transform keyframes and transitions
  * Shape layers: path vertices and transitions, path metadata
  * Nested layers

850 KB/face to ~1 KB/face! :)

Pain points?

* Android and web had to do more to get this to work (vs iOS)
* Bug where one particular Samsung chipset was doing some rendering optimization that made some parts of the face missing :P

### Intuit QuickBooks Self-Employed (Kristina)

* Mostly built using table views
* Built out a lot of generic UI views

Common components/generic views:

* Authorization Client (internal)
* Charts (external)
* OCR Receipt Capture (internal)

Cool focus on developer tools and productivity!

### Workflow iOS (Ayaka)

Company of six people!  
App lets people make workflows, kind of similar to IFTTT (but with more scripting actions?)

Structure

* Workflow
  * Main app
  * Houses all of our Swift code
* ActionKit, Interchangeable
* WorkflowUI
  * All of our reusable UI components
* WFLogging
  * Analytics via Mixpanel
* ContentKit
  * Manages our "content graph" (massages the data and tries to make it fit into a certain action)

By splitting up our app into different frameworks, it keeps things decoupled and our dependency graph simple. As we hire more people, it'll be easier to distribute our work.

### Pinterest (Wendy)

Infinite scrolling of pins!

Pin cells

* Image URL
* Title
* Pinner
  * User image URL
* Board

More complex cells = frame drops  
Moved to a new UI framework: AsyncDisplayKit

AsyncDisplayKit

* Usually UI work is confined to the "main thread"
* Using AsyncDisplayKit, we can initialize, configure, and layout views on background threads
* Serial > concurrent!
  * Now things must be thread-safe
  * Moved the app to an immutable model

How much can you control multithreading?

* Most iOS devices are multi-core
  * Most Pinterest iOS users have devices that can take advantage of multithreading
* Reduced app startup time by ~50% (plus moving more things to background queues)

Performance gains and how to measure them?

* Pinterest has a performance measurement framework, PinnerWaitTime (???)
* Things we track:
  * Time to render first screen of pins
  * Time for screen of search results to come back

## Q&A

### How has your codebase changed as your team has gotten larger?

* Kasia
  * Moving toward a more reusable backend
* Ayaka (at Venmo)
  * No one was really maintaining the app – there were tests but they were broken, there was no CI, etc.
  * In three years, now we had CI, tests, pull requests (rather than pushing to master), a lot more devs

### How do you make an app work well for users in all parts of the world?

* Jenny
  * One size solution doesn't work
  * Networking speed
    * For a while, the newsfeed was just a ListView
    * If you go into airplane mode, you'll still get a constant stream of stories
    * Creating much more offline support
    * Client-side ranking to give you stories that can be rendered more nicely
  * Old devices, old chipsets (emerging markets)
    * Facebook Light (???)
    * No client-side rendering
    * Takes a picture of the Facebook app and downloading it
    * Popular in Indonesia, India, etc.
* Kristina
  * Going through the globalization process right now
  * Localization for strings – German is ridiculous!
    * Working with writers to do key-value pairings for strings
    * Writers can directly commit to the codebase
      * At night, we run a script to pull the strings to compile into our beta app
      * Enables us to work faster

### Things we can do to keep accessibility in mind?

* Ayaka
  * Workflow got an Apple accessibility award for how accessible it is
  * Workflow is reducing the number of taps it takes so it's even better for visually impaired users
    * In contact with our visually impaired users
    * Beta testers who are visually impaired
  * JIRA tickets for making sure the app is accessible for each launch
* Jenny
  * Facebook Empathy Lab
    * Display of all of our apps, engineers can go and try them out with assistive technologies
  * Facebook is very image-rich
    * Automated captions/content descriptions for images
* Kristina
  * Not always just about visually impaired people
  * Keep in mind sound and haptic feedback (new feature in iOS 10)!

### Scalability of testing?

* Jenny
  * Snapshot tests
    * Unit tests for visual views
    * Instead of running end-to-end tests, it renders the views to a bitmap and compares the before and after
* Wendy
  * Testing on all types of devices and sizes
    * Zamarin (???)
    * Test device cloud
    * Tests are written in C# and run on all types of devices and models
* Kristina
  * Rainforest QA (manual testers)
* Ayaka
  * We rely a lot on our beta testers!

### React Native for app extensions?

* Kasia
  * This isn't something I've had experience with
  * What are the debugging problems?

### Why did you use React versus other options?

* Kasia
  * React was created at Facebook, so we have more control and access over that
  * Regressions tend to get solved immediately

### How do you get into mobile architecture? Any tips?

* Wendy
  * Looking at open source apps and common frameworks
  * Identifying common patterns
* Kristina
  * Going to conferences and hearing about best practices

### What did you find were your most transferrable skills working across multiple apps?

* Kasia
  * Switching from Android to React Native (especially for debugging iOS), but most mobile framework knowledge is transferrable
  * General debugging (related to programming in general)
* Jenny
  * What is the right way to allocate my time? Usually what we start out with is wrong – the first version probably won't work
  * Binary searching to a good solution is important
  * We ran >150 experiments for Reactions
  * How do you build an intuition for what users will like?
* Kristina
  * Intuit in four years, four different teams
    * Web > UX > Mobile
  * Understanding my customers and what they want at the end of the day
  * "Follow Me Home" – going to the customer's home and learn what they're dealing with and the problems they're having
  * Customer empathy

### How do you measure performance before release, or even before cutting the release build?

* Wendy
  * Xcode 6+ has performance testing (similar to writing unit tests)
  * Testing along "hot code paths"
    * Performance testing framework will run a block of code 10 times and then generate an average and standard deviation
    * If average rises too high or has too much variation, the test will fail
* Jenny
  * Android has a lot of devices!
  * None of our changes are shipped into the wild
  * Gatekeeper: will run 1% test first (~1 million people)
  * Using the alpha and beta channels (though mostly checking for crashes there)
