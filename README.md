# * Light and Sound Memory Game*


## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [X] Buttons use a pitch (frequency) other than the ones in the tutorial
* [X] More than 4 functional game buttons
* [X] Playback speeds up on each turn
* [ ] Computer picks a different pattern each time the game is played
* [X] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- An alert is popped up on the screen when the user makes a mistake, and it tells them that they have made a mistake and also how many strikes they have left till they lose. 
- After a mistake, the sequence is played back from the turn the user is on. 

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
1. Full Game Won:
![](http://g.recordit.co/ANuQqvzHsn.gif)
    Part 2 of Full Game Won: (Note: near the end some buttons are not captured by the gif because of the speed)
![](http://g.recordit.co/x51nrWL2UV.gif)

2. Mistake Alert shown and Game Over on Third Strike: 
![](http://g.recordit.co/SWMTTxcyhD.gif)

3. Different frequency sound of each button with audio: https://www.kapwing.com/videos/623ba00b49815200aa1ca860
![](https://media.giphy.com/media/egiFDhrOU6qKUues3N/giphy.gif)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
- w3schools.com

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
- I had a few challenges. The biggest one would probably be trying to figure out the guess function and how to progress through the game. I was able to come up with if the user guessed the correct button, and if the guess was incorrect, the user has lost the game. Which left my issue to be on how to progress through the game once the user guessed the correct button. But with the help of the given guess function I was able to somewhat understand it. I faced some challenges when trying to implement the optional features as well. I was able to figure out how to add new buttons and play around with the frequency of each button. But what stumped me was when I tried to speed up the clue playback. If I shaved too much time off, in the later turns, the clue playback would be way too fast to the point where the sound would not play and it was almost impossible to see what button was pressed. I essentially overcame this issue through trial and error, subtracting the clueHoldTime variable by different amounts until the last turn was really fast but still the user will be able to see and hear the clue. Another issue was when I tried giving the player 3 strikes until they lose instead of one chance to lose. Since I am still a little confused on the guess function it took me a while to understand how to update the guess function. But I realized I would only have to update the else where the player did not correctly guess the correct button and also create a check before calling the loseGame function. Since my variable mistake is initialized at 0, and the user has 3 strikes until they are out, the 3rd strike being game over, my check was if (mistake == 2), they will lose the game. And if the mistake does not equal 2, go to the else statement where I would update my variable mistake by 1 and also print out the number of mistakes the user has made so far. And if the user makes it to the third strike, the game is over, if not they win. 

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
- Some questions I would have just from this game would be how can I have a ranking system for different users? For example, the user that had the least amount of mistakes or finished the game the fastest, would be on the top of the ranking system. Also another question would be how do websites have a server or how would you create a server for your website? Something I’ve learned about from my Computer Science II class was concurrency. We didn’t discuss it much but I was wondering how multiple users can be on a website at the same time, and do different things at the same time? For example how can so many users be on amazon ordering different things at the same exact time and the website would do everything simultaneously? Which can lead back to this game, how can I have multiple players playing this game at the same exact time? 


4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
- If I had more time to work on this project, I would like to implement a difficulty setting where the user can decide which difficulty they want to play in. At easy level, the clue playback speed is the same speed all throughout the game and it's not fast and they have 5 strikes until game over. At normal level, the clue playback speed will increase a little as each turn progresses and the user will have 3 strikes until game over. Finally, at hard level, the clue playback speed is fast from the start and increases each turn and the user only has 1 chance. If they guess incorrectly, game over. 


## License

    Copyright Muhtasim Mushfiq

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
