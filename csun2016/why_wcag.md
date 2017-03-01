# Why WCAG? Whose Guideline is it, Anyway? with The Viking and The Lumberjack

Billy Gregory, Karl Groves

* [The Trouble with WCAG](#the-trouble-with-wcag)
  * [WCAG 2.0](#wcag-20)
    * [Can We Revise It?](#can-we-revise-it)
    * [Extend It?](#extend-it)
    * ["Exceptions"](#exceptions)
  * [What Bothers You About WCAG?](#what-bothers-you-about-wcag)
  * [Priorities vs Levels](#priorities-vs-levels)
  * [Success Criterion](#success-criterion)
* [Understanding WCAG 2.0](#understanding-wcag-20)
  * [POUR Principles](#pour-principles)
* [Conclusion](#conclusion)
* [Q&A](#qa)

## The Trouble with WCAG

It was released to be somewhat future-proof:

* Agnostic front-end
  * How do you validate native applications?
* "Leave No User Behind"
  * Consensus-based challenges, especially with low vision challenges

Phones have changed a lot. Tablets have become some users' primary device.

### WCAG 2.0

Started in 2000, released in 2008. 8 years!

#### Can We Revise It?

It's already been adopted into law internationally.

#### Extend It?

In the standards: "Extensions are optional standards modules…"

* Optional is NOT enough

It's already very long: 2000 pages printed! 8.5 x 11" paper = 22,000", 20 pounds of paper.

#### "Exceptions"

1.4.3 Contrast

* Except…if it is large text or incidental or logo

### What Bothers You About WCAG?

* Why is keyboard focus only AA?
* Podcasts need transcripts to be accessible – WCAG only applies to pre-recorded video.
* What does "normative" mean?
* Are native apps under web accessibility guidelines?

"WTF WCAG?!"

### Priorities vs Levels

We still don't know what they mean.

1.4.5 Images of Text (Level AA)  
2.4.7 Focus Visible (Level AA)  
2.4.10 Section Headings (Level AAA)

### Success Criterion

1.1.1 Non-Text Content

* If it isn't written text, you better have accessible content!
* We assume this is just about images, but it's not!
  * icon fonts
  * images of text
  * time-based media
  * inputs
  * controls
  * decorative/aesthetic images
  * CAPTCHA

Controls/inputs – should be 4.1.2  
Time based media – should be 1.2.1

1.3.1 Information and Relationships

* Structure your code properly
* Ensure you use the right elements
* Don't rely on style to convey meaning

1.3.2 Meaningful Sequence

* The order it appears on the screen is the way it should appear in your code
* We screw it up with tabindex!

1.4.1 Use of Color

* Don't ONLY use color to tell us stuff
* We think it means we can't convey information with color at all (but that's not the case)
  * Can use color AND text to highlight information
  * This also adheres to 1.3.1

## Understanding WCAG 2.0

* Do NOT read the entire document

### POUR Principles

1. Perceivable
2. Operable
3. Understandable
4. Robust

Map to the four sections of the guidelines.

## Conclusion

WCAG 2.0 is at least better than 508 (haha).

## Q&A

**There's a session after this with the WCAG working group. We welcome participation and feedback!**  
Thanks! The problem is that developers in a rush misinterpret things, and it's not that WCAG is terrible.

**It's hard to make a technical standard entertaining, and you've achieved that.**  
We've gotten mixed reviews! We did a talk, it was us making fun of accessibility, and people have different senses of humor. So thanks!
