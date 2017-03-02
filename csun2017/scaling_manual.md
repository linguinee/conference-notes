# Scaling Manual Accessibility Testing

Ian Kelly, Dequeue

* [Challenges](#challenges)
  * [Combinations and Fragmentation](#combinations-and-fragmentation)
* [Potential Solutions](#potential-solutions)
  * [Accessibility Requirements](#accessibility-requirements)
  * [Automation](#automation)
  * [Test While Developing](#test-while-developing)
  * [Provide Tools to Support Manual Testing](#provide-tools-to-support-manual-testing)

Enable designers and developers to produce the right content before they reach you! The broad theme of the Dequeue showcase this year is "shift left" – leverage the work of the team ahead of you.

## Challenges

Develpment is speeding up. Is QA disappearing? With the rise of agile and scrum, QA is working more closely with developers to write automation and integrate testing into development.

### Combinations and Fragmentation

* 4 operating systems, 2 supported versions
* 5 assistive technologies
* 4 browsers, 2 supported versions
* 3 responsive breakpoints

216 combinations excluding device combinations!

## Potential Solutions

* Accessibility requirements
* Enable the team to test themselves
* Automate what you can
* Provide tool support for manual testing

### Accessibility Requirements

Annotate UX wireframes with accessibility information

* What role do the UI elements have?
* What order should the content be read in?
* What is the structure of the page?
* Keyboard interaction?

### Automation

* Use browser extensions
* Embed into unit tests
* Embed into integration tests
* Catch ~40% of accessibility defects

### Test While Developing

* Make sure everything works with the keyboard
* Make sure it works with a screen reader
* Write automated tests for a11y requirements

(WorldSpace Attest)

### Provide Tools to Support Manual Testing

Manual testing challenges: consistent findings, complete coverage, and efficiency.

Experiment: 9 accessibility experts, 1 complex page, test to WCAG 2.0 AA, unlimited time. One person took 1 hour to find 4 issues, another took 8 hours to find 30+ issues, another took 4 hours to find 30 issues. The results were all over the place.

(WorldSpace Assure)

**Q&A:** How does Assure differ from aXe?  
Assure is built on top of the aXe rules engine.
