# Transforming Novices into Skilled Accessibility Testers with a 3x3 Process

Mark Stimson, Kaiser Permanente

* [Objective](#objective)
* [The Problem](#the-problem)
* [Our Experience](#our-experience)
  * [KP's Digital Experience](#kps-digital-experience)
    * [KP's Digital Inclusion](#kps-digital-inclusion)
* [Scaling](#scaling)
  * [Why do Testers need to cover accessibility?](#why-do-testers-need-to-cover-accessibility)
  * [Why is training Testers difficult?](#why-is-training-testers-difficult)
* [KP's Epiphany](#kp-s-epiphany)
  * [Mobile App Project](#mobile-app-project)
  * [Defects fell into 2 patterns…](#defects-fell-into-2-patterns)
    * [Apply to VoiceOver testing](#apply-to-voiceover-testing)
  * [Developed 3x3 matrix](#developed-3x3-matrix)
    * [Training](#training)
    * [Results](#results)
  * [Transforming to Web in General](#transforming-to-web-in-general)
* [Summary](#summary)

www.linkedin.com/in/drmarkstimson

Small accessibility team of three people at Kaiser Permanente.

## Objective

Share Kaiser Permanente's proven method of transforming novice QA testers into skilled screen reader testers. Not talking about eliminating accessibility specialists – we're talking about scaling.

## The Problem

Large organization with few Accessibility SMEs (specialists).

* Compliance is a must!
* Not enough skilled workers to succeed
* Cannot hire your way out
* Training Accessibility SMEs takes time

## Our Experience

Kaiser Permanente is the largest care and coverage health care organization – a non-profit offering lowest cost with best care. 7 regions in 8 states with 82 hospitals and 622 medical offices. 10,250,000 members, 17,000 doctors, 175,000 employees.

### KP's Digital Experience

History

* Began in 1996
* Integrated into first large-scale EMR (electronic medical records)
* Care integrated digitally (appointments, visits, Rx, labs, records, preventions, etc.)

Now

* 70% of members registered on kp.org
* Half-million visits/day
* Majority from mobile

#### KP's Digital Inclusion

Section 508 in 2003, WCAG 2.0 in 2013.

## Scaling

You need to scale. All necessary teams need to have Accessibility skills:

* Accessibility SMEs
* Designers
* Developers
* Testers

### Why do Testers need to cover accessibility?

* A couple a11y SMEs cannot test everything
* QA/PQ Testers
  * Have product knowledge
  * Have access or credentials
  * Aligned to know the what, where, and when of testing
  * Aligned with development to communicate and log defects

### Why is training Testers difficult?

* Mostly contractors
  * Max of 2 years, average 8 months
  * No accessibility background
* WCAG 2.0 is dense and technical
  * Level A, AA (37 standards)
  * Best Practices (192 criteria)
* Functional testing with screen readers like JAWS can take a long time to learn

## KP's Epiphany

### Mobile App Project

* iOS was a game changer
* Usability was unprecedented
* Allows sighted people to use apps without sight
* Defects can fit into a much simpler categorization strategy
* Maybe this can be the way of onboarding Testers

### Defects fell into 2 patterns…

* Most defects could be mapped to one WCAG standard (~95%)
  * WCAG 4.1.2: "Name, Role, Value"
  * e.g. dimmed submit button
    * Expected Behavior: VoiceOver speaks "Submit button, dimmed"
    * Name = "Submit"
    * Role = "Button"
    * Value = "Dimmed"
* These defects also can fit into 1 of 3 categories for CC testing
  * Error Classes
    * In testing closed captioning accuracy, errors can be categorized in one of three ways
      * Substitution
      * Deletion
      * Insertion

#### Apply to VoiceOver testing

The Name, Role, or Value can fall into…

* Substitution: VoiceOver reads a name, role or value
* Omission: Expected is omitted
* Insertion: VoiceOver reads a tahat is not on the screen, and not expected

### Developed 3x3 matrix

|                  | Name | Role | Value |
|------------------|------|------|-------|
| **Substitution** | S2   | S2   | S2    |
| **Omission**     | S1   | S2   | S1    |
| **Insertion**    | S2   | S2   | S2    |

Severity values can increase or decrease based on context. If user *cannot* recover, then increase severity level. If user *can* easily recover, then decrease severity level.

#### Training

We trained a 4 person team of scrum testers to:

* Use VoiceOver gestures
* Interpret VoiceOver speech
* Learn what is expected

#### Results

* Team was able to test entire app (several thousand tasks)
* QA Testers discovered 140 defects
* 95% of defects found by QA Testers using the 3x3 approach
  * Other 5% found by a11y SMEs – more advanced things like color contrast, error messages, etc.
* Defects were found early enough so that only three Severity 3 defects remained

### Transforming to Web in General

* Take advantage of "Mobile First"
* iOS app testing can be adjusted to work for web testing
* Testers learn slight differences in expectations for Web vs. App
* QA Testers also perform automated testing
* A11y SMEs assist with more in-depth testing

## Summary

1. Scaling accessibility is essential
2. QA Testers can be the most challenging to onboard
3. Take advantage of "Mobile First"
4. Simplify the tools and process
5. Mentor the Testers and provide additional SME testing as necessary
