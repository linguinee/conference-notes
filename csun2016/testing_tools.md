# Accessibility Testing Tools for Developers

Gerard Cohen

* [Basic Testing](#basic-testing)
  * [HTML Validation](#html-validation)
  * [Keyboard Focus with TAB](#keyboard-focus-with-tab)
* [Bookmarklets](#bookmarklets)
  * [CSS Bookmarklets](#css-bookmarklets)
    * [Custom Rules](#custom-rules)
  * [JS Bookmarklets](#js-bookmarklets)
* [Browser Plugins](#browser-plugins)
* [Advanced Testing](#advanced-testing)
* [Q&A](#qa)

[Slide deck](http://www.slideshare.net/gerardkcohen/accessibility-testing-tools-for-developers-gerard-k-cohen-csun-2016)  
Test site: http://fyvr.net/acme/

## Basic Testing

### HTML Validation

**W3C HTML Checker** https://validator.w3.org/nu/  
Validate markup plus suggestions for ARIA roles.

**Web Developer Tools** http://chrispederick.com/work/web-developer/  
Extension adds various web developer tools to the browser.

**Local Validator** https://github.com/validator/validator  
If you're behind a firewall – or for privacy reasons.

### Keyboard Focus with TAB

Make sure focus is flowing in a natural order. Look for keyboard traps and hidden elements. When you get to the bottom, Shift+Tab and make sure the reverse works, too.

CSS debugging:

```
/* Helps locate focus */
:focus {
  border: 1px solid red;
}
```

Also look for improper tab index values – only proper values are -1 and 0.

## Bookmarklets

### CSS Bookmarklets

**debugCSS** http://yahoo.github.io/debugCSS/  
Developed by Yahoo. Tests accessibility, tables, namespace, and other HTML checks.

**Diagnostic.css** http://www.karlgroves.com/2013/09/07/diagnostic-css-super-quick-web-accessibility-testing/  
Developed by Karl Groves. Tests for deprecated elements, images without alt attributes, empty TITLE elements, etc.

**Revenge.CSS** https://github.com/Heydon/REVENGE.CSS  
Developed by Heydon Pickering.

#### Custom Rules

Defensive CSS!

e.g. CSS Toolbar "Widget" checks for role="group" and aria-label="some-label" – it pops up a warning bubble if either of them are missing. This is in production code!

```
.toolbar:not([aria-label]),
.toolbar[aria-label=""] {
  position: relative;
}

.toolbar:not([aria-label]):before,
.toolbar[aria-label=""]:before {
  background-color: #dc143c;
  color: #fff;
  content: "A11y: Unique aria-label missing.";
  font-size: 1rem;
  left: 0;
  padding: 0.625rem;
  position: absolute;
  top: -2.875rem;
}
```

### JS Bookmarklets

**Tota11y** http://khan.github.io/tota11y  
Developed by Khan Academy.

**HTML CodeSniffer** http://squizlabs.github.io/HTML_CodeSniffer  
Developed by Squiz.

## Browser Plugins

**Web Developer Tools** http://chrispederick.com/work/web-developer/  
Developed by Chris Pederick. Remove CSS, highlight headings, etc.

**Accessibility Developer Tools** (in the console)  
Developed by Chrome.

* Inspector > highlight element > Accessibility Properties
    * Will give color contrast, plus a color combination that you can use!

**WAVE** http://wave.webaim.org/extension/  
Developed by WebAim.

**aXe** http://www.deque.com/products/axe/  
Developed by Deque.

**Tenon** http://tenon.io/  
Developed by Karl Groves. Similar to HTML Validator. There is a self-hosted solution (if it's a privacy violation).

## Advanced Testing

Experiment to build accessibility into end-to-end testing using Selenium, Node.js, and some plugins (e.g. Nightwatch, Tenon, etc.): https://github.com/gerardkcohen/nightwatch-a11y-testing

## Q&A

**Any automation that you know about to test tab? Looking for keyboard traps (e.g. autocomplete) or focus lost. Like we need to 1) have a generic tabbing function that can be used over and over again and 2) come together as an industry to define tabbing for tabpanels and there are standardized rules so that someone could just give the test function the xpath of the tabpanel.**  
Good questions – currently my tests are specific to the web page and pretty brittle.

**What about making sure certain colors aren't together, for people who are colorblind (e.g. red on black)?**  
Our designers are pretty good at that!
