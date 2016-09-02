# Simon | UBC Launch Pad JavaScript Interview Project

Thank you for choosing to interview with us and welcome to the UBC Launch Pad JavaScript interview project! The purpose of this interview stage is to give you a chance to demonstrate your programming abilities in a more relaxed environment than an in-person interview. You can choose to try either the Easy Task, the Challenge Task, or both. If you aren't able or don't have time to complete it, we still encourage you to apply with what you _have_ done.

Note: We recommend using Google Chrome when developing this project. Other browsers may not have as robust a Web Audio implementation (looking at you, Safari).

We have provided you with audio files, a skeleton HTML file linking to the audio files and containing four coloured note boxes, a CSS file styling the note boxes, and a JavaScript file which implements an interface to these note boxes. The note boxes are buttons that play a note and light up when activated. The JavaScript file contains a constructor for creating NoteBox objects, which are used to interact with and control the note boxes.

The NoteBox object exposes several public methods for you to use in this project.

`NoteBox#constructor` - Accepts a `key` parameter and an optional `onClick` parameter. The `key` should be the ID of note box element on the page. `onClick` is a handler function that is called when the note box is clicked, if it is enabled.

`NoteBox#play` - Activates this NoteBox by lighting it up and playing its corresponding note, regardless of whether or not it is enabled.

`NoteBox#enable` - Enables this NoteBox so that clicking it will trigger it lighting up and playing its corresponding note.

`NoteBox#disable` - Disables this NoteBox so that clicking it will accomplish nothing.

## Easy Task

Implement a NoteBox "echo" application. Whenever the user plays one of the NoteBoxes by clicking it, after a duration of 2.5 seconds, you should echo whatever note the user played back to them. If they play multiple notes with less than 2.5 seconds between each note, you should wait them to finish (i.e. not play a note for 2.5 seconds), then play back the sequence they played.

## Challenge Task

Implement the game [Simon](https://en.wikipedia.org/wiki/Simon_(game)) using JavaScript and the NoteBox interface we have provided. If you don't know how the game works, take a look at the Wikipedia article or [play it yourself](http://www.kidsmathgamesonline.com/memory/simon.html).

There is no need to replicate the look of the original (although you can if you want). What we are looking for is a replication of the basic functionality of the game, with the note boxes described above being isomorphic to the buttons in Simon. Specifically, your implementation should randomly generate a note to begin the game, and play it in the corresponding note box. Then it should wait for the user to select a note and verify that it matches the randomly generated note. Then it should randomly generate a new note to append to the previous note in the sequence and play the sequence. Then wait for the user to select notes matching the sequence. And so on until the user selects an incorrect note. Your implementation should immediately detect when the user deviates from the sequence by selecting an incorrect note, and should immediately restart the game.

## Rules

1. You are allowed to use code from external sources (i.e. Stack Overflow), but try to avoid it for more than one or two lines. If you do use code from an external source, you should link to the source in a comment.
2. Don't ask your friends for help. This project should be done on your own.
3. You _can_ alter the provided `NoteBox`, but in general you should add to it rather than replacing it.

## Submission

Fork this repository into your personal GitHub account and do your work there, then link to your version in the application form. When you are finished, we should be able to clone your repository and see your work by running an HTTP server in the root project folder.

Create a file called `NOTES.md` and note any significant difficulties you had while completing the tasks, anything you would like to explain about your code, how you approached and solved the problem, or what resources you used. Think of this as analogous to explaining your code during an in-person interview coding question. You can write as little or as much as you want. Good luck :)
