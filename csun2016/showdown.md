# Automated Testing Tool Showdown

Luis Garcia

* [Analysis Method](#analysis-method)
* [Preliminary Overall Findings](#preliminary-overall-findings)
  * [Unique Findings](#unique-findings)
* [General Accessibility Tools Overview](#general-accessibility-tools-overview)
  * [Accessibility Developer Tools Overview](#accessibility-developer-tools-overview)
  * [AInspector Sidebar Overview](#ainspector-sidebar-overview)
  * [aXe Overview](#axe-overview)
  * [WAVE Overview](#wave-overview)
* [Next Steps](#next-steps)

Slides: http://www.garcialo.com/tools/presentation/

## Summary

**Why a tools talk?**

* I use accessibility tools every day
* I hadn't really analyzed the tools themselves
* Prefer topics targeted to those newer to accessibility

**Inclusion Criteria**

* Free
* Easy to use
* Fairly robust
* Local Analysis

**Tools List**

* http://www.garcialo.com/tools/
* Additional tools that have been talked about in a previous presentation
* Additional tools are less automatic or require more work to get going
* [HTML Codesniffer](http://squizlabs.github.io/HTML_CodeSniffer/), [WAVE Online](http://wave.webaim.org/), and [Tenon.io](http://www.tenon.io/) removed for lack of local analysis

## Analysis Method

**What to look at?**

* Based on WCAG 2.0
* Looking at success criteria that can be found by automated tools
  * 30-45% can be automated, humans need to look at the other ones
* Examine bad examples of accessibility
* Objective features of each tool

**Which rules to check?**

* For which success criteria does each tool have at least one test?
* Which tools uniquely check for which success criteria?
* What percentage of success criteria are checked by each tool?
* [Automated Tools Data Page](http://www.garcialo.com/tools/toolsdata.html)

**Challenge:** Automated tools produce false positives. If you want zero false positives, there will be less automated tests and more manual testing needed.

**Examples of ****Bad Accessibility**  
[a11yNot](http://www.a11ynot.com/) site renders Bad Examples and track which tools catch which Bad Examples.

**Problems with Analysis Method**

* Mapping of checks to success criteria may be inaccurate/incomplete
* Many WCAG failure techniques can only be found by manual check
* Bad Examples might not have been implemented correctly
* Bad Examples might not actually be bad; haven't all been manually verified
* Bad Examples are not comprehensive for all checks for each tool
* Documentation of which tools find which issues might not be accurate

## Preliminary Overall Findings

**WAVE and AInspector**  
Issues found by WAVE and AInspector not found by aXe and Accessibility Developer Tools.

* Elements with onClick events
* Heading misuse

**aXe and Accessibility Developer Tools**
* Found more ARIA-specific issues

### Unique Findings

**AInspector**

* Focus-related issues
  * e.g. focus indication issues
* Autosubmitted forms
* Elements with onClick events

**aXe**

* Meta refresh (using meta element to do refresh on the page itself)
* Table-related issues (found table issues better than the other tools)
* Misuse of role="presentation"
  * e.g. layout table with role="presentation", you shouldn't be using tbody, thead, etc. because it implies that it's a data table – you should only be using td's and tr's

**WAVE**

* "spacer" images
* Pays attention to CSS/style for more than just contrast
  * alignment
  * blink
  * etc.

## General Accessibility Tools Overview

### Accessibility Developer Tools Overview

http://www.garcialo.com/tools/presentation/devtools.html  
http://www.garcialo.com/tools/presentation/devtools-continued.html

### AInspector Sidebar Overview

http://www.garcialo.com/tools/presentation/ainspector.html  
http://www.garcialo.com/tools/presentation/ainspector-continued.html

### aXe Overview

http://www.garcialo.com/tools/presentation/axe.html  
http://www.garcialo.com/tools/presentation/axe-continued.html

### WAVE Overview

http://www.garcialo.com/tools/presentation/wave.html  
http://www.garcialo.com/tools/presentation/wave-continued.html

## Next Steps

**Include Other Tools in Analysis**

* Open AJAX Accessibility Extension
* HTML Codesniffer
* Tenon.io

**Minimize/Mitigate Problems with Analysis Method**

* Manually verify inaccessibility of Bad Examples
* Create additional Bad Examples to cover all checks for each tool
* Investigate additional Bad Example repositories mentioned by Wendy Chisholm
