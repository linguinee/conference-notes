# Accessibility at the intersection of visual design and front-end development

Mitchell Evan, SSB BART Group

* [Challenge #1: Color Contrast of Text](#challenge-1-color-contrast-of-text)
  * [When should color contrast happen?](#when-should-color-contrast-happen)
  * [Process and design buy-in](#process-and-design-buy-in)
    * [Inclusive design](#inclusive-design)
* [Challenge #2: Keyboard Access](#challenge-2-keyboard-access)
  * [Useful facets of keyboard accessibility](#useful-facets-of-keyboard-accessibility)
  * [Testing](#testing)
  * [Responsibilities](#responsibilities)
* [What's Next?](#whats-next)

Two challenges today (which I would argue are symptoms of organizational dysfunction):

## Challenge #1: Color Contrast of Text

Remediation may not be obvious…

Example of a horizontal list of links where one link is selected and the others are unselected. The designer says, the unselected links are disabled so they don't need to meet color contrast guidelines!

Possibilities, together or separately:

* Change the text colors
* Change the background color
* Change the font size or weight
* Add a non-color visual indicator

**Design problem:** You improve legibility, but you lose the visual statement of which link is selected.

### When should color contrast happen?

* Very early
  * Design ideation
  * UI architecture
  * Accessibility strategy
* Systems
  * **Design system  ← good time to fix color contrast issues**
  * UI components
  * Iterative support
* Build
  * Design production
  * Primary development
  * Iterative support
* Quality Assurance
* Release

### Process and design buy-in

Talk to each other and decide on the plan!

* The designer is mainly responsible
* Choose a testing methodology and tool
  * Do you use the CSS hex color or use an eyedropper on the text?
  * Make a solid plan to fix early in a design cycle

#### Inclusive design

Always ask who is excluded!

## Challenge #2: Keyboard Access

One particular way of breaking up keyboard accessibility and answering the question of who is going to work on what, in terms of tasks for a software or web team.

### Useful facets of keyboard accessibility

* Tab order
* Focus management for in-page updates
* Visual focus indication
* Keystrokes to select or activate

### Testing

**All UI developers should know how to do this with a keyboard ("quick test"):**

* Tab and Shift+Tab
* Arrow or Space to select
* Enter or Space to activate
* Visual focus indication on all tabbable elements
* Logical focus location at all times

*Audience note: Conformity, consistency, uniformity of a layout, especially for people with brain injuries (cognitive disabilities and/or visual disabilities), is important!*

**Stress test with expert testers:**

* Desktop sighted keyboard
* Desktop screen readers
* Mobile sighted keyboard
* Mobile screen readers with keyboard
* Dragon Naturally Speaking

### Responsibilities

Mitchell's take on this:

* Tab order
  * Developer mainly responsible, Designer and A11y Specialist involved
* Focus management
  * Developer mainly responsible, A11y Specialist mostly responsible, Designer involved
* Visual focus indication
  * Designer mainly responsible, Developer involved
* Select or activate
  * A11y Specialist mainly responsible, Developer mostly responsible

## What's Next?

Real visual examples – what are some great resilient designs?

Examples for discussion (no endorsement):

* Chase
* Yahoo! News Digest

Keep asking: who is excluded?
Talk to each other.

Decide on the plan.

* Who is responsible?
* What are the testing methodologies?
* What's the plan for the project lifecycle?

