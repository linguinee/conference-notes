# ARIA prerequisites: What You Need to Know Before Implementing ARIA

Jonathan Whiting, WebAIM

* [ARIA](#aria)
* [ARIA Prerequisites](#aria-prerequisites)
  * [First Rule of ARIA Use](#first-rule-of-aria-use)
    * [Why aren't developers aware of this?](#why-arent-developers-aware-of-this)
  * [Accessibility APIs](#accessibility-apis)
    * [ARIA Roles](#aria-roles)
    * [Accessible Names](#accessible-names)
  * [ARIA Documentation](#aria-documentation)
  * [Screen Reader Testing](#screen-reader-testing)
* [Q&A](#qa)

## ARIA

"To ARIA: the cause of, and solution, to all our accessibility problems!"

How do we fix it?

* Better tools/frameworks/libraries
* Better education on using ARIA
* **Better prerequisite education before using ARIA**

## ARIA Prerequisites

What do developers need to know before they even start using ARIA?

* HTML accessibility
* Accessibility APIs
* ARIA documentation
* Screen reader testing
* Others???

### First Rule of ARIA Use

If you can use HTML, then do so.

The first rule of ARIA is, if you can, don't use ARIA.  
"Just use a button!!!"

[Notes on Using ARIA in HTML](https://www.w3.org/TR/aria-in-html/)

#### Why aren't developers aware of this?

* Developers haven't learned about accessibility
* Web developers are learning HTML through bad examples
* "Use a button" – "Okay, `<span class="button">`"
  * Maybe we should change to say, "Use a native HTML button"?
* If things are already built, ARIA is used to fix it
* ARIA is more rich than HTML, e.g. sliders

### Accessibility APIs

Accessibility APIs are channels that pass accessibility information on. For example, screen readers should get accessibility information through the browser and OS.

```
<input type="checkbox" value="sprouts" id="sp">
    <label for="sp">Sprouts</label
```

Role: checkbox  
Label: Sprouts  
State: checked

ARIA does not change browser behavior! ARIA changes accessibility APIs…which can change screen reader behavior.

#### ARIA Roles

ARIA roles **win**.

```
<input type="checkbox" value="sprouts" id="sp" role="radio">
    <label for="sp">Sprouts</label
```

Role: **radio button**  
Label: Sprouts  
State: checked

Now the screen reader tells the user to interact with the radio button with arrow keys (rather than using SPACE on checkboxes)! But ARIA hasn't changed the browser behavior at all.

Opinion: What's the most abused ARIA role?

* button
* menu

#### ARIA States/Properties vs HTML

HTML wins, except:

* When HTML isn't playing
* When ARIA is disqualified
* When you use an ARIA label
* Other rules I can't figure out

```
<input type="checkbox" value="sprouts" id="sp" aria-checked="false">
    <label for="sp">Sprouts</label>
```

Role: checkbox  
Label: Sprouts  
State: checked

```
<input type="checkbox" value="sprouts" id="sp" aria-describedby="risk">
    <label for="sp">Sprouts</label>
<div id="risk">The consumption of raw sprouts…</div>
```

Role: checkbox  
Label: Sprouts  
State: checked
Description: The consumption of raw sprouts…

#### Accessible Names

ARIA **labels** override accessible **names**.

* Alternative text
* Link text
* Button text
* Form labels

```
<input type="checkbox" value="sprouts" id="sp" aria-label="Pick 3 veggies">
    <label for="sp">Sprouts</label>
```

Role: checkbox  
Label: Pick 3 veggies  
State: checked

**Question:** What about using `aria-labelledby` and referencing an id for the label instead?  
I recommend `aria-label` over `aria-labelledby` since you lose the ability to click on the name to check the checkbox, which is a larger click/touch target.

### ARIA Documentation

[ARIA Authoring Practices](https://www.w3.org/TR/wai-aria-practices-1.1/)
* Authoring Practices – Design Patterns
* Notes – 5 Rules
* ARIA in HTML – Document Conformance Requirements

Just use ARIA Design Patterns!!!

### Screen Reader Testing

Screen reader shortcuts

| Command           | NVDA/JAWS                           | VoiceOver          |
|-------------------| ------------------------------------| -------------------|
| "Special" key     | Insert                              | Ctrl + Option + VO |
| Read all          | Insert + Down Arrow                 | VO + A             |
| Read one line     | Down Arrow                          | VO + Arrow         |
| Stop reading      | Ctrl                                | Ctrl               |
| Links/form fields | Tab                                 | Tab                |
| Headings          | H, 1-6                              | VO + Cmd + H       |
| Forms             | F                                   | VO + Cmd + J       |
| Tables            | T                                   | VO + Cmd + T       |
| "Rotor"           |                                     | VO + U + Arrow     |
| Landmarks         | D (NVDA), R (JAWS 15), ; (JAWS < 5) | Rotor              |

## Q&A

**In the university setting, I've discouraged unnecessary use. I've used examples as a way to show good practices – do you have more suggestions for examples?**  
All of the big accessibility groups have good examples. The authoring practices ones are probably the best, and more selective from the pool of examples, too.

**I've found that the most challenging thing is the vernacular and how ARIA is translated by browsers. Do we forget VoiceOver a little bit more than JAWS, or…?**  
I think the more you can stick to the ARIA specifications. A more common screen reader like NVDA is better for ARIA testing than VoiceOver.

**My developers don't know what focus is. It's been a big roadblock for us.**  
It's definitely a prerequisite, yes, good point.
