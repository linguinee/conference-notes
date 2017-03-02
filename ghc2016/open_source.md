# Navigating and Contributing to Large-Scale Open Source Projects

Beth Dakin, Apple

* [Overview of the WebKit Code](#overview-of-the-webkit-code)
* [Getting Involved](#getting-involved)
  * [Early Contributions](#early-contributions)
    * [Report (good) bugs](#report--good--bugs)
      * [The Anatomy of a Good Bug Report](#the-anatomy-of-a-good-bug-report)
    * [Create reduced test cases](#create-reduced-test-cases)
    * [Track down regressions](#track-down-regressions)
    * [Write test cases](#write-test-cases)
  * [Contributing Patches](#contributing-patches)
    * [Walk before you run](#walk-before-you-run)
    * [A patch is just the beginning](#a-patch-is-just-the-beginning)
    * [Communication is key](#communication-is-key)
    * [Add a test with your patch!](#add-a-test-with-your-patch-)

## Overview of the WebKit Code

Stack:

* WebKit and WebKit2
* WebCore
  * Load, render, and interact with a webpage
  * The largest section
* JavaScriptCore
  * Compilers, garbage collection, JS as a language
* WTF
  * Lists, sets, etc.
* bmalloc

Clang and Swift → LLVM Optimizer → LLVM Code Generator → exec ↔ compiler-rt

## Getting Involved

### Early Contributions

#### Report (good) bugs

* Test against the latest version of software
* Safari Technology Preview (STP) – put out every two weeks

##### The Anatomy of a Good Bug Report

* Clear description of the problem
  * "Safari crashes in WebPage::dictionaryPopupInfo() clicking the comment button at http://mysneakywebsite.com/blog"
* Include the version of the browser and OS
* Series of steps that anyone can follow to reproduce the problem
* Description of expected and actual behavior
* Crash log (if applicable)

#### Create reduced test cases

A web page or small program that reduces the bug!

#### Track down regressions

Go to nightly builds and find when the bug occurred.

#### Write test cases

Tests are important!

### Contributing Patches

#### Walk before you run

* Keywords or labels: GoodFirstBug, StarterBug, etc.
* Email or IRC
* Find the right people!

#### A patch is just the beginning

Code reviews, continuous integration, etc.

#### Communication is key

Get on IRC, chat rooms, etc.

#### Add a test with your patch!

The best way to show that you've fixed the bug :)
