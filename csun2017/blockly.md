# Accessible Blockly: Making a Visual Coding Environment Accessible

Cory Diers, Kevin Chao, and Yi-Yi Kung, Google

* [Blockly](#blockly)
  * [Accessible Blockly](#accessible-blockly)
    * [Why is there an Accessible Blockly?](#why-is-there-an-accessible-blockly)
* [UX Research](#ux-research)
  * [UI Challenges](#ui-challenges)
    * [Results](#results)
    * [Updates](#updates)
* [Next Steps](#next-steps)
* [Q&A](#qa)

This is a talk that Cory presented on work that Kevin, I, and many other people at Google have been working on!

## Blockly

Blockly is a library for creating visual programming editors for kids. It relies on blocks and connecting blocks together to form programs, which is often easier to start with than text-based languages, where beginning users can have a lot of syntax errors.

Question: How might we make a **highly visual** UX design, like the one in Blockly, accessible to those who are visually impaired?

### Accessible Blockly

Additional library that sits on top of Blockly.

* Tutorial levels
* Music game to teach sequential for loops

#### Why is there an Accessible Blockly?

* With a visual interface dependent on drag-and-drop blocks, Blockly doesn't translate well to a purely audio- or keyboard-based interface
* Accessible Blockly allows us to explore other ways of teaching and understanding coding concepts
* Updates to Blockly also propagate to Accessible Blockly
  * Being conscious of problems associated with "separate but equal" accessible programs

## UX Research

Students from the California School for the Blind came and tried out the music game.

### UI Challenges

* Moving blocks from the toolbox to the workspace
* Instructions: need to be clear but non-verbose
* In the workspace, is there one island or multiple islands?
  * Are the blocks all connected together, or are they separate?
* Orientation: how do students know "where they are"?
  * Telling the difference between whether one is in the toolbox or workspace

#### Results

Challenges

* Kids weren't as familiar with using screen readers than we expected them to be
* Kids struggled with navigating the tree structure of the interface
* Kids had trouble understanding the relationship between the components of the interface
* Kids seemed to struggle with the three-column design and the copy/paste metaphor

Feedback

* Auditory music component of the game was very useful for kids to hear if they had correctly written their program

#### Updates

With these results, we created a tutorial game that teaches kids how to move within the tree structure using a screen reader. The student needs to navigate through a house with various rooms and items in it, represented by a tree structure, in order to find a cat.

We also moved more actions to modal, context-dependent dialogs, in order to de-clutter the screen and make it easier for kids to only interact with one thing at a time.

## Q&A

**One of the useful things about Blockly is shape-matching to syntax. For example, the "if" block is a C shape that looks like it can contain other blocks.**  
We haven't explored how to translate that into audio, but it's definitely something to look into.

**Have you done anything with making Blockly work with Arduino? Scratch does.**  
I don't see anything that would prevent it from working with Arduino.

**Have you done anything with tactical displays to use Blockly as Blockly?**  
I think it's a great idea, and something that we haven't looked into yet.

**You said you had studied six students? What was the age range?**  
11-14 in the first group, and 10-17 in the second group.

**Was it the younger students who had more trouble using screen readers?**  
Yes, mostly students in the 10-13 age range.

**Have you considered using college student screen reader users?**  
The age range for Blockly is older elementary and younger middle school students, though Blockly does aim to be as general purpose as possible. It isn't something we've looked into, but we'd love to see more use with people in other age ranges.

**What happens when someone makes an error in configuring a block?**  
The nice thing about Blockly is that it shouldn't have any compilation errors. Usually when you make a mistake in a program, you'll hear it, in Accessible Blockly. So an errors should be obvious when you run the code.

**Is Accessible Blockly all HTML? Have you thought about doing a native app?**  
Accessible Blockly is all in HTML. Traditional Blockly is a web app, and there are mobile apps, but they're in active development.

**Does this work well in Chrome?**  
Yes – there are a couple of bugs in a couple of screen readers, but we've been figuring them out. The demos were in Firefox with NVDA on Windows.
