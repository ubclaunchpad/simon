# Simon | UBC Launch Pad JavaScript Interview Project

Thank you for choosing to interview with us and welcome to the UBC Launch Pad JavaScript interview project! The purpose of this interview stage is to give you a chance to demonstrate your programming abilities in a more relaxed environment than an in-person interview. There are two tasks in this project, the Junior Task and the Senior Task. You will complete the Junior Task if you are interviewing for the Junior Developer position and the Senior Task if you are interviewing for the Senior Developer position (but you're more than welcome to try out the Senior Task as a Junior if you'd like).

We have provided you with audio files, a skeleton HTML file linking to the audio files and containing four coloured note boxes, a CSS file styling the note boxes, and a JavaScript file which implements an interface to these note boxes. The note boxes are buttons that play a note and light up when activated. The JavaScript file contains a constructor for creating NoteBox objects, which are used to interact with and control the note boxes.

The NoteBox object exposes several public methods for you to use in this project.

`NoteBox#constructor` - Accepts a `key` parameter and an optional `onClick` parameter. The `key` should be the ID of note box element on the page. `onClick` is a handler function that is called when the note box is clicked, if it is enabled.

`NoteBox#play` - Activates this NoteBox by lighting it up and playing its corresponding note, regardless of whether or not it is enabled.

`NoteBox#enable` - Enables this NoteBox so that clicking it will trigger it lighting up and playing its corresponding note.

`NoteBox#disable` - Disables this NoteBox so that clicking it will accomplish nothing.


## Junior Task

Your task is to implement the game [Simon](https://en.wikipedia.org/wiki/Simon_(game)) using JavaScript and the NoteBox interface we have provided. If you don't know how the game works, take a look at the Wikipedia article or [play it yourself](http://www.kidsmathgamesonline.com/memory/simon.html).

There is no need to replicate the look of the original (although you can if you want). What we are looking for is a replication of the basic functionality of the game, with the note boxes described above being isomorphic to the buttons in Simon. Specifically, your implementation should randomly generate a note to begin the game, and play it in the corresponding note box. Then it should wait for the user to select a note and verify that it matches the randomly generated note. Then it should randomly generate a new note to append to the previous note in the sequence and play the sequence. Then wait for the user select notes matching the sequence. And so on until the user selects an incorrect note. Your implementation should immediately detect when the user deviates from the sequence by selecting an incorrect note, and should immediately restart the game.

## Senior Task

Your task is to implement the Simon game as described in the Junior task description, but with some additional requirements.

1. Add a Start button that starts the game. When the game is in progress, it should become a Reset button, resetting the game to the initial state.
2. Add a "You lose" alert/popup/notification when the user loses and tell them the length of their longest correct sequence of notes. The alert should contain the option to reset the game (with the same behaviour as #1) or to replay.
3. Require the user to replicate the sequence within a certain (reasonable) period of time, otherwise they lose. This time should be reset each time the user selects a next note box.
4. Increase the rate at which the randomly generated sequence is played for the user at each round. For instance, if Round 4 (with 4 notes) is played with an interval of 800ms between each note, then play Round 5 with an interval of 700ms between each note.

## Rules

1. You are allowed to use code from external sources, but do not copy more than 5 consecutive lines of code from someone else (i.e. Stack Overflow). If you do use code from an external source, you should link to the source in a comment.
2. Don't ask your friends for help. This project should be done on your own.
3. You _can_ alter the provided `NoteBox`, but in general you should add to it rather than replacing it.

## Submission

Fork this repository into your personal GitHub account. Then create a new branch called `simon`. Complete the tasks above in the `simon` branch. When you are finished, we should be able to clone your repository and see your work by running an HTTP server in the root project folder.

Create a file called `NOTES.md` and note any significant difficulties you had while completing the tasks, anything you would like to explain about your code, how you approached and solved the problem, or what resources you used. If you were unable to complete some of the tasks, explain why in the `NOTE.md` file as well. Think of this as analogous to explaining your code during an in-person interview coding question. Finally, push your changes to your fork of this repository and let us know that you're done. Good luck :)
