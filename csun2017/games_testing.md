# How the BBC is Changing Games Testing Through Accessibility

Hannah Bunce, BBC

* [Games at Children's BBC](#games-at-childrens-bbc)
* [The Problem](#the-problem)
* [Solutions](#solutions)
* [Future Work](#future-work)
* [Q&A](#qa)

## Games at Children's BBC

HTML5 games for children 2-12:

* CBeebies (2-6)
* CBBC (6-12)

## The Problem

Something Special: The Looking Game (target age: 2-4)

* Hidden object game
* Designed to be screen reader friendly
* Colorblind friendly version (red, green and blue buttons also change shape)

User complaint that it couldn't be accessed using iOS/VoiceOver. The final build that we'd received before release had broken screen reader functionality! It had come in three hours before the game was about to go live.

New game: Playtime Island

* HTML5 games can be downloaded on the phone and played there
* Testing games on the web and on the phone
* Doubled our QA requirements, since web and app testing are separate

## Solutions

* QA is part of the design and development process
* Documentation!
  * Children's Games Accessibility Guidelines & Recommendations
  * Accessibility test cases as part of the manual test case suite

The 4 C's:

* Collaboration
  * QA and UX, e.g. designing a game for children with autism
  * QA and external vendor, e.g. auditing > 300 games for switch access
* Champion accessibility at all levels
  * "Accessibility Champions" throughout the BBC
* Consistency
  * Consistent forms of communication and processes around accessibility
* Communication
  * Open communication lines across the board, e.g. between the games team and apps team

No more external user reports about accessibility on our games!

## Future Work

* More research
* More training
* Maintaining documentation
* Working groups
  * Accessibility Champion Testers working group – swap tips and tricks, meet up monthly
  * Increases knowledge and skill sharing
* Emphasizing communication
* Review processes on a regular basis
  * Once every 2-3 months
  * Tried reviewing processes every 2-3 weeks, but that was too fast of a turnaround

## Q&A

**Automated testing?**  
There is an accessibility testing automated framework within the BBC, but we've found that it wouldn't be useful for our own work.

**Catching bugs earlier?**  
We've found that reviewing the games as soon as possible has reduced the number of bugs and caught them earlier.
