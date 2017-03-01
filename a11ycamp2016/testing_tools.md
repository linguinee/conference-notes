# Accessibility Testing Tools for Developers

Gerard K. Cohen  
[@gerardkcohe*n](https://twitter.com/gerardkcohen)  
gerardkcohen@gmail.com

* [Basic Tests](#basic-tests)
  * [HTML Validation](#html-validation)
  * [Tab Key](#tab-key)
* [More Tests](#more-tests)
  * [CSS Bookmarklets](#css-bookmarklets)
  * [JS Bookmarklets](#js-bookmarklets)
  * [Browser Plugins](#browser-plugins)

Slides: https://goo.gl/0f4wQH  
Nightwatch Checker: https://github.com/gerardkcohen/nightwatch-a11y-testing

## Basic Tests

### HTML Validation

Nu Html Checker

* https://goo.gl/xqZnhw
* https://validator.w3.org/nu/

Web Developer Tools

* https://goo.gl/EzdK
* http://chrispederick.com/work/web-developer/

Local Validator

* https://goo.gl/1v5ZDI
* https://github.com/validator/validator

### Tab Key

* Tab through a page
* When you get to the bottom, shift+TAB back through the page

```
/* Helps locate focus */
:focus {
  border: 1px solid red;
}

JS console: document.activeElement
```

## More Tests

### CSS Bookmarklets

debugCSS

* https://goo.gl/1Q6wEA
* http://yahoo.github.io/debugCSS/
* http://imgrainj.github.io/debugCSS/

Diagnostic.css

* https://goo.gl/9h1FEI
* http://www.karlgroves.com/2013/09/07/diagnostic-css-super-quick-web-accessibility-testing/

Revenge.CSS

* https://goo.gl/81oI6p
* https://github.com/Heydon/REVENGE.CSS

a11y.CSS (new one added this year)

* https://goo.gl/s34e3d
* https://ffoodd.github.io/a11y.css/

### JS Bookmarklets

Tota11y

* https://goo.gl/IPGAj6
* http://khan.github.io/tota11y/

HTML CodeSniffer

* https://goo.gl/umvAEP
* http://squizlabs.github.io/HTML_CodeSniffer/

### Browser Plugins

Web Developer Tools

* https://goo.gl/EzdK
* http://chrispederick.com/work/web-developer/

Chrome Accessibility Developer Tools

* https://goo.gl/KUZDzs

Chromelens

* https://goo.gl/oTw5Gi

Tenon

* http://tenon.io/

a11yTools Extension for Safari

* https://goo.gl/0KnOzO
* http://pauljadam.com/extension.html
