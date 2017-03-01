# Reduce Accessibility Coding Costs: Nudge Developers with Linters and Types

Jesse Beach and Tatiana Iskandar, Facebook

* [Facebook Web Accessibility](#facebook-web-accessibility)
* [Accessibility Impact](#accessibility-impact)
  * [Strong Typing](#strong-typing)
    * [Strong typing in JavaScript](#strong-typing-in-javascript)
    * [ARIA smarts in React.js](#aria-smarts-in-reactjs)
    * [Strong typing in XHP](#strong-typing-in-xhp)
  * [Linting](#linting)
    * [eslint-plugin-jsx-a11y](#eslint-plugin-jsx-a11y)
  * [Codemodding](#codemodding)
  * [Code Review](#code-review)
  * [Invest in Components](#invest-in-components)
  * [Support Your Champions](#support-your-champions)
  * [Automate Teaching](#automate-teaching)
  * [Bootcamp](#bootcamp)
* [Tips](#tips)

## Facebook Web Accessibility

"Accessibility Maintenance Crew" ← this probably sounds familiar to most people!

Facebook is really big and really busy. Nothing is required, and new tools appear all the time. The accessibility team has remained small, < 10 people.

We can't just grow the headcount of the team – we must grow the **impact** of the team.

## Accessibility Impact

Why don't we have time to focus on innovation?

**Problem:** Too few experts
  * Minimal or no accessibility development knowledge
  * Countless simple errors

**Solution:** Make every dev an expert! Integrate guides with developer tools.

What are the common errors? What can we know at code time, specifically?

### Strong Typing

#### Strong typing in JavaScript

* Type the falues for ARIA role attribute
* [Flow](https://flowtype.org/), static type checking

```
export type ARIACompositeWidgetRole = 'combobox' | 'grid' | listbox' | 'menu' | 'menubar' | 'radiogroup' | 'tablist' | 'tree' | 'treegrid';
```

#### ARIA smarts in React.js

* Warns against invalid aria-* attributes
* https://github.com/facebook/react/pull/7744

#### Strong typing in XHP

* XHP, it's like HTML in PHP

After all these improvements, why don't we still have time to innovate?

Still too few experts! Typing has a limited reach.

### Linting

Contextual feedback *before* code gets committed

* ESLint
* JSLint
* JSHint

Testing "food pyramid": Manual tests > End to End Tests > Integration Tests > Unit Tests

We see linting rules as the base of this pyramid! More abstract than tests in your system, shareable across products and organizations.

#### eslint-plugin-jsx-a11y

* https://github.com/evcohen/eslint-plugin-jsx-a11y
* ARIA Query (modeling the ARIA spec)
  * https://github.com/a11yance/aria-query
* Link rule violations to documentation
* Just JSX right now

After all these improvements, why don't we still have time to innovate?

Too much to fix!

### Codemodding

* Lets us fix the same problem across multiple files all at once!
* Labeled over 700 buttons
* Fixed > 2,000 linting violation
* https://github.com/facebook/jscodeshift

Why codemodding now?

* Two years ago, we didn't have:
  * Extensible parsers (Babylon, TypeScript)
  * Community focus on AST defintiion development
  * Usable pretty-printers (Recast)
  * User-friendly modding library (JSCodeshift)

### Code Review

* Auto-subscribe to accessibility diffs
* Tag-team accessibility code reviewing
* Praise authors!

After all these improvements, why don't we still have time to innovate?

Too many solutions!

* Unnecessary solutions
* Insufficient solutions
* We can't keep up!

Most UIs at Facebook are constructed from components, so most accessibility bugs can be traced back to inaccessible components.

### Invest in Components

* Support library authors
* Build abstract components and behaviors
* Mark components as accessible and inaccessible in the UI Component Explorer
  * Currently components are marked manually
  * In the future, looking to automate this

After all these improvements, why don't we still have time to innovate?

Too many regressions! AX team can't fix all of the issues.

### Support Your Champions

* Provide documentation (wiki)
* "A11y Rallies" instead of training
* Provide support

After all these improvements, why don't we still have time to innovate?

Too many teaching moments! Following up on tasks takes time.

### Automate Teaching

* Clearly document our UBN/Hi/Mid/Lo criteria
* Categorize tasks based on tags/descriptions
* Milo Bot
  * Facebook tool that performs maintenance on tasks
  * Automatically comments on tasks with information like links to documentation
  * Comments when tasks are downgraded in priority (don't ignore accessibility!)

After all these improvements, why don't we still have time to innovate?

Too little awareness! New developers are unaware of accessibility and unaware of our team.

### Bootcamp

* 6-8 week training for new eng hires
* Over 200 "add a label" tasks
* Accessibility awareness
* Milo Bot links them to the getting started guide!

## Tips

* Win back your time through automation
* Prevent simple issues with linters
* Fix common errors through codemodding
* Getting support from peers to advocate for accessibility
* Design reusable solution through components
* Spread awareness through onboarding tasks

Celebrate!
