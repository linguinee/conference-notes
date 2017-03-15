# Automatica11y: Past, Present and Future of Automated Tooling

Job Van Achterberg

* [Testing](#testing)
  * [Tooling types](#tooling-types)
* [Older Tools](#older-tools)
* [Current Tools](#current-tools)
* [Browser Extensions and Plugins](#browser-extensions-and-plugins)
* [APIs](#apis)
* [Hopes for the Future](#hopes-for-the-future)
  * [Better Tests](#better-tests)
  * [More Heuristics](#more-heuristics)
  * [Increased Integrations](#increased-integrations)
  * [Framework Specificity](#framework-specificity)
  * [More Configurability](#more-configurability)
  * [Component Testing](#component-testing)
  * [Walled Garden Testing](#walled-garden-testing)
  * [Project Management Integration](#project-management-integration)
  * [More CSS Heuristics](#more-css-heuristics)
* [Resources](#resources)

## Testing

Test for compliance, usability, and regression.

There's a lot of black box testing, but what about unit testing?

### Tooling types

* Online checkers
* Browser extensions/plugins
* APIs
* Libraries

## Older Tools

* CAST Bobby
* Cryptzone Cynthia Says
* AChecker (still available)

## Current Tools

* Nu HTML Checker
* WebAIM WAVE
* aXe
* Tenon.io
* Readable.io (readability)
* Juicy Studio

## Browser Extensions and Plugins

* WebAIM WAVE
* ContrastRatioChecker
* Color Contrast Analyzer
* NoCoffee Vision Simulator
* Chrome Developer Tools
* TRAY Readability Tool

## APIs

* Tenon.io
* WAVE API
* Validator.nu API

## Hopes for the Future

Analyzed data from webdevdata.org and found an increase in uses of \<section\>, \<header\>, role attribute usage, WAI-ARIA usage, etc.

Out of 3,692,336 images, 27% has no alt text. 16% has empty alt text. Top five after that? 'S', 'M', 'L', 'D', ''.

People are still using aria-live="rude". Wrong role usages, like "accessibleItem", "accordion", "body", "facebook"…??

In the future: analyzing websites to determine what underlying frameworks were used to produce accessibility errors.

### Better Tests

* Correct ARIA usage
* Proper semantics
  * Suggestions or hints on role usage
* More in-depth, like screen flicker detection
  * Take screenshots at different times and diff them
* Contrast, visibility detection

### More Heuristics

* Machine learning image alt text (e.g. Facebook)
* Semantic suggestions

### Increased Integrations

* CI systems (e.g. Jenkins)
* Trackers (e.g. GitHub, JIRA)
* Other APIS (e.g. Readability.io)
* Plugins (e.g. Sketch, MS Office)
* Programming editors and IDEs

### Framework Specificity

We've become siloed and accessibility has become more specific to the framework you're using.

* ngAria
* react-a11y
* ember-a11y

### More Configurability

* Show me only some errors/warnings when I'm developing
* Show me everything when a build fails
* Don't bug me about this because [reason]

### Component Testing

More and more we're developing components to be used as part of a web page. We should be testing these as components.

### Walled Garden Testing

* What if we can't get out?
* What if we need to authenticate?
* Deploy locally?
* Containerised service?
* What about paid services?

### Project Management Integration

* Track a11y as part of the roadmap
* Measure regression (tracker integration)
* Measure impact of features on a11y
* Measure a11y impact on velocity

### More CSS Heuristics

* Absolute units
* Control font sizes
* Click targets
* Hover style and focus style
* Outline vs custom outline detection
* etc.!

## Resources

* [GDS Audit](https://alphagov.github.io/accessibility-tool-audit)
  * How do automated accessibility checkers compare?
