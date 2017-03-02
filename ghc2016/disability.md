# Disability is a Design Problem

Elise Livingston (elise.livingston@gmail.com, [@elivingston3](https://twitter.com/elivingston3))  
Program Manager, Microsoft (accessibility driver for most of the Microsoft Suite)

* [Inclusive Design](#inclusive-design)
  * [Disability](#disability)
    * [What is disability?](#what-is-disability)
    * [Disability is a spectrum](#disability-is-a-spectrum)
    * [Innovation begins with disability](#innovation-begins-with-disability)
    * [Mobile and Ubiquitous Technology](#mobile-and-ubiquitous-technology)
* [Case Study: Assist](#case-study-assist)
    * [Accessibility](#accessibility)
    * [Assistive Technologies (ATs)](#assistive-technologies-ats)
* [Strategies and Tools](#strategies-and-tools)
    * [Accessibility Test Plan](#accessibility-test-plan)
* [Key Takeaways](#key-takeaways)
* [Q&A](#qa)

## Inclusive Design

* Thinking about accessibility in the design process
* Inclusive design is NOT an all-in-one solution
* Inclusive design means options
  * We don't need one screwdriver to fit all the different screws in the world, we need a bunch of screwdrivers!

### Disability

* 1 in 7 people worldwide have a disability
* 70% of disabilities are not immediately apparent

#### What is disability?

* We now recognize disability as not just a health problem, it's "a complex phenomenon, reflecting the interaction between features of a person’s body and features of the society in which they live"
* A mismatch between the abilities of a person and the capability of a product.

#### Disability is a spectrum

* **Permanent:** one arm
* **Temporary:** arm injury
* **Situational:** new parent, carrying groceries, holding onto a bus pole

**Disability is something that we design into our products.**

#### Innovation begins with disability

* Typewriter
* Email
* Skype Translator

#### Mobile and Ubiquitous Technology

More mobility in technology means more contexts of use, and that means more moments of disability.

## Case Study: Assist

"UX for Good" Project

* How might we help someone with a vision impairment navigate an unfamiliar building accurately and confidently?
* UX Research: Surveys, interviews, literature review, competitive analysis, etc.
* After talking with blind and visually impaired users, we realized that they felt like a burden on their friends and family – the question changed:
  * How might we help someone get assistance quickly in any new situation?

### Accessibility

Accessibility is a set of tools that provide options for people with varying ability.

### Assistive Technologies (ATs)

* Screen readers
  * Narrator, VoiceOver, JAWS, Window Eyes, NVDA, TalkBack
* Screen adjustment settings
  * ZoomText, Magnifier, Zoom, High Contrast
* Speech input
  * Dragon Naturally Speaking, Dictation, Speech Recognition
* Keyboard
  * Sticky Keys, Mouse Keys, Filter Keys, Keyboard Shortcuts

## Strategies and Tools

Consider:

1. Who might be excluded from using my feature?
2. How will my feature work with assistive technologies?

### Accessibility Test Plan

Screen

* Test your feature in all OS High Contrast settings on all platforms
* Test your feature on OS screen magnification tools

Keyboard

* Make sure all functions of the feature are accessible via keyboard only without requiring simultaneous input

Screen Reader

* Turn on Narrator, VoiceOver, etc.
  * The name, role, and value/state of every piece of UI is communicated clearly
  * All feature functions can be completed, and are sufficiently described by the screen reader

## Key Takeaways

1. Disability is a mismatch between the abilities of a person and the capability of a product.
2. Inclusive innovation often comes from designing for permanent disability in mind.
3. Always ask:
  * Who might be excluded from using my feature?
  * How will my feature work with assistive technologies?

## Q&A

**What accessibility features have you audited?** 
I've done a lot of work in making sure – we own a lot of the graphical components – so helped people understand advanced formatting, that this shape is blue, how the layout of a slide is, etc.

**Finding colors with the right contrast ratio has been hard. How do you balance when design should be accessible versus having users rely on accessible technology?**  
You should always be exposing as much information as you can, e.g. if they have to know this thing is blue, you should convey that to them. It also depends on the tools that you make, since with Office we want to make sure that it's easy for people to make sure the things they create are accessible.

**How do you make sure accessibility is implemented from the start?**  
It's a culture change thing, and you kind of have to be the advocate there. I've given presentations to the team – people have asked me if they can ship without something and I say no.
