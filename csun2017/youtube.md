# Closed Captions and Subtitles at YouTube

Caile Collens, YouTube  
Noah Wang, Google Accessibility

* [Viewer Experience](#viewer-experience)
  * [Caption shortcuts](#caption-shortcuts)
* [Video Uploader Experience](#video-uploader-experience)
  * [Creator Tools](#creator-tools)
  * [Crowdsourcing](#crowdsourcing)
  * [Automatic speech recognition](#automatic-speech-recognition)
* [Announcements](#announcements)
  * [Sound effects in automatic captions](#sound-effects-in-automatic-captions)
* [Q&A](#qa)

## Viewer Experience

* Customizable caption styling on your desktop
  * Font family (including sans serif or serif), font color, font size, background color, etc.
  * Style settings should be saved from video to video
* Captions are draggable to different parts of the screen
  * Caption location will also be saved
  * Good for things like newscasts, where captions can block the lower portion of the screen

Learn more on the [YouTube Help Center](https://support.google.com/youtube).

Did you know? The CC badge is shown for human-authored tracks available in the language of your UI.

### Caption shortcuts

* 'b' will toggle the background shading on or off
* '+' makes the captions bigger
* '-' makes the captions smaller

## Video Uploader Experience

Multiple ways to create captions on YouTube!

### Creator tools

Different methods:

* Uplaod a file
  * .srt, WebVTT, etc. all supported
* Transcribe and auto-sync
* Create new subtitles/CC
* Buy subtitles/CC or translation

### Crowdsourcing

Turn on community contributions (default off) for one or all of your videos.

### Automatic speech recognition

Words with less opacity (e.g. grey on black versus white on black) have less confidence that they're correct.

Auto-generated caption tracks can also be edited. When you do this, it'll no longer appear as automatic – it'll be listed as English and not English (auto-generated).

## Announcements

Improved speech recognition quality for English! Reduced error rate by half over the last year.

### Sound effects in automatic captions

  * Applause, music, and more to come
  * Rolling out in English and other languages
  * First production system that automatically adds sound effects?

Key findings

* Sound effects are more effective for "invisible" sound information
  * Not very effective when sound information is visually available
* Sound effects are more effective when sound infromation is not available
  * Misleading wrong caption may detract UX

Potential improvements

* Combined audio-visual analysis (increase sound effect *informativity*)
* Improved precision on recognition (increase sound effect *accessibility*)

## Q&A

**Are the crowdsourced captions moderated in any way?**  
Crowdsourced caption tracks are ultimately owned by the video owner, so they can edit, delete, and moderate the captions.

**Is there a way to request crowdsourced comments to be turned on?**  
There's no button on the video player to request crowdsourced comments to be turned on, but that's good feedback. Creators are also pretty responsive to comments, so that's a way to ask them to turn those on.

**Are the caption settings keyboard accessible?**  
We have three keyboard shortcuts for background color and size, and the settings menus are keyboard accessible. However, dragging the captions is not keyboard accessible.

**As a creator, can I download caption files?**  
When you have captions available on YouTube, you can download them as .srt files.

**Is there a time cut-off for automatic captions?**  
We don't have a strict cut-off. It's hard to say because it depends on a lot of factors.

**Is there a way to upload another audio track for audio descriptions?**  
Currently, no, but it's one of our top feature requests, and we'll note that in the feedback.

**If you're uploading your own transcript with no timings, are there any tricks to help it along?**  
It won't take any line breaks into consideration, but it should take sentence breaks into consideration to some extent.

**How does automatic captions handle accents?**  
Very generally. We have a wide variety of inputs in our training data, and it's really dependent on the individual in relation to the training data. It also depends on background noise in the video

**Is there support for livestreaming?**  
Yes, if you're livestreaming, you can have live captions through a closed captioner.

**If a video won't have auto-generated captions, how does the video creator know that?**  
There's currently not an overt feedback mechanism for that. If it's been a day, then there probably won't be automatic captions. There's not a direct amount of time that auto-generated captions will take, since it depends on how complex the sound in the video is. But if it's been a day, there probably won't be automatic captions.

**Following up on that, do you have a best practices guide to ensure auto-generated captions?**  
Eliminating background noise, a microphone for people speaking, etc. It only deals with one language per video, as well.

**With the YouTube API, it's hard for third-party players to turn captions on and off. Was that intentional?**  
Not to my knowledge, but we'll put that down as feedback for the team responsible.

**If your video has captions, will that affect search results?**  
I'm not sure if search takes into account captions or caption contents at all.

**How did you decide on the default caption styling?**  
I'm not sure, that was a choice made before I joined the team. However, creators can specify colors and caption placement through .srt files. This can't be done through the Creator Studio right now, but YouTube will take formatting into account for uploaded caption files.

**Has the caption creation process been tested for accessibility?**  
Yes, user-facing products at Google have all been tested for accessibility.

**Can we have more up-to-date videos and tutorials for creating captions?**  
Yes! Feedback is being recorded for this.
