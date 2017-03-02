# Advanced ARIA

Harris Schneiderman, Deque

* [Overview](#overview)
* [ARIA Best Practices](#aria-best-practices)
  * [Live Regions](#live-regions)
* [Examples](#examples)
  * [Dragon Drop](#dragon-drop)
  * [Toggle Buttons](#toggle-buttons)
  * [Modal Dialog](#modal-dialog)
  * [Mega Menu](#mega-menu)
  * [Checkboxes](#checkboxes)

## Overview

With ARIA, we can provide attributes/values that are consumable by assistive technology to provide more context.

**Role:** what the element is  
**State:** the current state of the element  
**Property:** essential attributes of the nature of the element (less likely to change than states)

In the real world, many websites aren't designed with accessibility in mind.

ARIA to the rescue!

* Best solution is to use native button and link elements
* Quickly/easily fix legacy content
* No modifying HTML tag structures

Modern screen readers have excellent WAI-ARIA support.

## ARIA Best Practices

Use native elements when possible!

Challenging situations:

* Dynamic content that updates in remote parts of the page
* Interactive widgets that alter states of their components
* Datepickers
* Carousels
* Custom controls (radio and checkbox)
* The list goes on

Things to remember:

* Roles/states/properties
* Label
* Focusable/keyboard operability
  * Desktop web apps
  * Don't forget about mobile!
* For mobile – touch operability
* Follow the spec according to the role
* Color contrast
* For custom controls: [Custom Control Accessible Development Checklist](https://w3c.github.io/aria-in-html/#checklist)

### Live Regions

ARIA Live Region is a tool that can notify screen readers of content changes.

* Realtime updates about remote parts of the page
* Status updates
* Announce time sensitive information

Examples:

* Chat logs
* Server status updates (connection lost)
* Confirmation messages
* Progress indicators

Live regions should be used sparingly as they can easily createa verbose experience for screen reader users!

Live Region Playground  
https://schne324.github.io/live-region-playground/

## Examples

### Dragon Drop

Re-order a list using only the keyboard!  
http://harris-schneiderman.com/demos/dragon-drop/index.html

### Toggle Buttons

* Must be keyboard operable (focusable and activatable)
* Pressed state toggled by activation

NOTE: the label of a toggle button must not change when the state changes (confusing!)

* SPACE/ENTER should toggle the state
* Ideally a native button element, or `role="button"`

### Modal Dialog

* When the dialog trigger is clicked, focus shifted to modal dialog
* When the dialog is closed, return focus to the trigger

Keyboard interaction should take care of TAB, Shift + TAB, and ESCAPE.

`role="dialog"` and `aria-label="Label"`  
or  
`aria-labelledby="id of label"`

Don't forget about aria-hidden! Apply aria-hidden="true" to all elements except for the modal itself. This will prevent screen readers from being able to traverse outside of the dialog.

### Mega Menu

* When a submenu is opened, focus should be shifted to the first menu item
* When a submenu is closed, focus should be shifted to the parent menu item that triggered the opening of the submenu

Keyboard interaction needs to take care of ENTER and Down, Up, Right, and Left Arrows.

Try to avoid dual purpose menu items – those that both perform an action AND trigger a submenu.

`role="menubar"` (top-level menu)  
`role="menuitem"` (child menu items)  
`role="menu"` (on the submenus)  
`aria-haspopup="true"` (has a submenu)

Mega Menu Example  
http://mattisner.com/a11y-examples/menu/

### Checkboxes

* Clicking, pressing space bar, and tapping (mobile) should toggle the checkbox
* Needs an accessible label (recommended: visible label associated via `aria-labelledby`)
* `aria-checked="true"` when toggled on
