# Common Accessibility Testing Mistakes

Natalie Patrice Tucker, Edward Miller

* [Coding Mistakes](#coding-mistakes)
  * [Checkboxes](#checkboxes)
  * [Mishandling form errors](#mishandling-form-errors)
  * [Missing or poor labelling](#missing-or-poor-labelling)
  * [Creating unusable forms](#creating-unusable-forms)
  * [Incorrect use of data table structures](#incorrect-use-of-data-table-structures)
  * [Using controls that do not support AT](#using-controls-that-do-not-support-at)
  * [Incorrect use of accessibility attributes](#incorrect-use-of-accessibility-attributes)
  * [Incorrect use of Headings](#incorrect-use-of-headings)
  * [Failure to provide support for keyboard-only users](#failure-to-provide-support-for-keyboard-only-users)
* [Summary](#summary)

(got to the session a bit late!)

## Coding Mistakes

### Checkboxes

Associate label with checkbox.

### Mishandling form errors

* What is wrong?
* Where is the error?
* How do I fix it?

### Missing or poor labelling

* Placeholder text in place of labels
  * Screen reader users and users with cognitive impairments are affected because it's hard to remember what the form is for.
* Poor color contrast
  * Users with low vision are affected because it's hard to read the text.

### Creating unusable forms

* Use visible label text
* Provide support for groups of form controls
* Communicate constraints: required, character limit
* Give the user help when submission fails: what, where, how

### Incorrect use of data table structures

e.g. Using a data table to layout a form.

* Data tables should only be used to present tabular data

```
<form>
<table>
  <tr><th scope="row">Your name</th>
    <td><input type="text" name="name" size="20">
    <td></tr>
  </tr>
…
```

### Using controls that do not support AT

* Use ARIA to provide missing accessibility information
* Ensure that web controls have the Name, Role, and State to correctly identify them
* Ensure that web controls provide the functionality and user interactive experience the user is expecting from the control
  * Especially important for keyboard users.

### Incorrect use of accessibility attributes

* Combining attributes
  * alt
  * title (isn't reliably supported by all browsers and AT!)
  * aria-label
  * aria-labelledby
* Redundant < Accessible

### Incorrect use of Headings

Headings should be in order!

### Failure to provide support for keyboard-only users

* Mouse enabled actions do not support keyboard actions
* Minimal or no visible focus indicator with keyboard

## Summary

Planning:
* Identify the standard(s) for your team
* Investigate development framework's support for accessibility

Remember:

* Use the right attribute or approach
* Test with users, code review, use automated testing, test with assistive technology
