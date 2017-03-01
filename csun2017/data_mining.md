# Data-Mining Accessibility: Research into Technologies to Determine Risk

Karl Groves and Nater Kane, Tenon.io

How do you figure out if something has terrible accessibility before you use it?

The total time (and cost!) to find a bug, fix it, and verify it is too much. Let's just avoid it.

## Tenon R&D

* Users in every timezone, in 113 countries
* Users have run > 1 million API calls against 26,698 distinct domains
* Logged > 50 million errors
* We can use this information for good

What do we know?

* Total errors logged: 50,769,881
* Max errors/warnings on a page: 6,539/5,629
* Average errors: 25
* Standard deviation (errors): 79
* Percentage of tests passing: 94%

## Methodology and Goals

We know three important things:

* High-level statistics
  * Pass vs fail, % of errors by WCAG level, etc.
* Issue details
  * Including issue category, severity, impacted
* Technologies in use

AWS S3 was down, so they'll run the query today and post on the blog with the results tomorrow.
