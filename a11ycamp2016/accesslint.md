# Pragmatic Accessibility Testing in CI with AccessLint

Cameron Cundiff, ThoughtBot, [@ckundo](https://twitter.com/ckundo)

* [AccessLint](#accesslint)
  * [Command Line Demo](#command-line-demo)
  * [Developer Tool Demo](#developer-tool-demo)
  * [Why AccessLint?](#why-accesslint)
* [How It Works](#how-it-works)
  * [What's next?](#whats-next)
* [Questions?](#questions)

Slides: http://tinyurl.com/accesslint-slides

## AccessLint

A suite of developer tools for pragmatic accessibility testing.  
https://github.com/accesslint

* Web-based
  * AccessLint applies JavaScript tests (from the axe-core library) for WCAG and Section 508 violations
* Developer-centric
  * AccessLint CI is (mostly) based on command line tools, CI, and GitHub workflows.

### Command Line Demo

1. Start web server
2. Install AccessLint's command line tool
  * Takes arguments and the URL you want to evaluate
3. Run the command line tool (crawls the page and finds accessibility errors!)
  * e.g. accesslint-ci scan --skip-ci http://localhost:4567
4. Get the results!

### Developer Tool Demo

1. Add the bot as a collaborator to your github repo
2. Commit change and push it to a branch on github
3. Open a pull request on github
4. Build runs on CircleCI
5. Accessibility checks run and any accessibility errors surface as a comment on github

### Why AccessLint?

* "DRY" – don't repeat yourself
  * Automation takes a load off of developers and makes tasks more asynchronous
* Be transparent
  * Thoughtbot has a tradition of open source projects and knows the benefits (and costs) of maintaining open source software
* Good command line tools do one thing
  * Each component has a single responsibility, which means we can chain tools together to make interesting things
* Ask, don't tell
  * Application development is a conversation, accessibility included

Some of these opinions might be controversial, especially in terms of not failing the build for accessibility errors.

## How It Works

axe-core

* https://github.com/dequelabs/axe-core

accesslint.js

* https://github.com/accesslint/accesslint.js
* Runs axe-core in a page and logs errors on in the browser console, both on page load and on DOM mutation events

accesslint-cli

* `npm install -g accesslint-cli`  
`accesslint https://www.thoughtbot.com`
* Run axe-core on a page in a headless browser from the command line

accesslint-ci

* `gem install accesslint-ci`  
`accesslint-ci scan https://www.thoughtbot.com`
* Crawl a host site and run accessibility assertions on the pages
* If there are any new accessibility issues, accesslint-ci will comment on the pull request that initiated the build in CircleCI

### What's next?

* Hosted logging and comments (accesslint.com)
* Package manager (Homebrew)
* Production analytics

## Questions?

**Right now, it's only running on CircleCI. What are the barriers to get it to run on other CI?**  
We currently store the logs in Circle's artifacts. In this case, we're coupled to CircleCI because that's what we use. We have it queued up to store the logs in S3 so that our service can deal with everything and make it agnostic to the platform.

**What about an option to ignore specific URLs? What about a configuration file for the project such as with lint?**  
I worry about blacklisting circle pages because they might never get removed from the list. I like the second option better. With the configuration options, you could say that some things don't reply, e.g. saying that you only care about critical errors. We could have a YAML file where you specify the rules you want to run.

**What about ignoring a specific failure in the logs? Specific to a selector and a rule?**  
This is why commenting rather than failing the build is better. I've learned that just marking things as inaccessible is not a good way to get developers to change things.

[Introducing AccessLint CI - Automated Web Accessibility Testing](https://robots.thoughtbot.com/introducing-accesslint-web-accessibility-testing-in-ci)
