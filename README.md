# 'Stop the Hatter-Moles' Start Document

| Version | Description      | Date       |
| ------- | ---------------- | ---------- |
| 0.1     | Interim Document | 02/06/2021 |



## Introduction

### Game Description

> Stop the hatter Moles is a fun and addictive reaction game about fighting off the evil Hat moles' attack and getting the highest score. Be sure to be very attentive as those devious creatures can push a bomb under your hammer, which will end your defense in 3 miss-clicks. 

Jump right into this fun game here

#### Interim Mockups

| Desktop Mockup                                               |
| ------------------------------------------------------------ |
| ![](https://github.com/AlekseiSkr/HatMoles/blob/a4977111ac06c14806ea03d9267abd60ab79e3d9/Documentation%20Assets/game.png) |
| Mobile Mockup (Maybe)                                        |
| ![](https://github.com/AlekseiSkr/HatMoles/blob/a4977111ac06c14806ea03d9267abd60ab79e3d9/Documentation%20Assets/iPhone%206,%207,%208%20Plus%20%E2%80%93%20scoreboard.png) |



## Input / Output / Assets

### Input 

| Input                                            | Type                  | Condition                                                    |
| ------------------------------------------------ | --------------------- | ------------------------------------------------------------ |
| Pressing the start button to start the game      | Button Click          | The game has to be in the initial state, and not in the playing state. |
| Pressing on the Mole to hit it with a hammer     | DOM Element selection | The Mole has to be visible                                   |
| Press Ok on the death screen to agree with death | Button Click          | Lives left = 0                                               |

### Output

| Output     | Type   | Condition                            |
| ---------- | ------ | ------------------------------------ |
| Score      | Number | Game is in the started/playing state |
| Time Left  | Number | Game is in the started/playing state |
| Lives Left | Number | Game is in the started/playing state |

### Proposed Technology

| Technology         | Purpose                                                      |
| ------------------ | ------------------------------------------------------------ |
| **JQuery**         | Complete DOM control as the game will be developed in the WEB |
| **Javascript**     | Dom control and building responsive features,                |
| **HTML** **/ CSS** | Building the Front-End                                       |

#### External Technology 

##### [Simple Bulk Image Resizer](https://bulkresizephotos.com/en)

- Is an image bulk resize website service, which will assist in sizing images for use as Sprites

### Sprites 

![](https://github.com/AlekseiSkr/HatMoles/blob/a4977111ac06c14806ea03d9267abd60ab79e3d9/Documentation%20Assets/Group%2010.png)

### Background

![](https://github.com/AlekseiSkr/HatMoles/blob/a4977111ac06c14806ea03d9267abd60ab79e3d9/Documentation%20Assets/game%20%E2%80%93%20back.png)

## UML Class Diagram

//![](https://github.com/AlekseiSkr/HatMoles/blob/a4977111ac06c14806ea03d9267abd60ab79e3d9/Documentation%20Assets/UML%20class.jpeg)



## Tests

| Test case /  Purpose                                         | Precondition                          | Impact | Trigger                                      | Postcondition                                                |
| ------------------------------------------------------------ | ------------------------------------- | ------ | -------------------------------------------- | ------------------------------------------------------------ |
| As a user I want to start a game with a button press         | Game state = menu                     | High   | Pressing Start button on the top of the view | The game starts                                              |
| As a user I want the game to end upon reaching the time limit | timer left time <= 0                  | High   | Timer runs out of time                       | A window pop-up and tells you that the game is ended         |
| As a user I want the game to end upon reaching 0 lives left  | Lives left = 0                        | High   | Run out of lives                             | A window pop-up and tells you that the game is ended         |
| As a user I want to see my score after the game has ended    | Game state = ended                    | High   | Run out of lives / Timer runs out of time    | A window pop-up and tells you that the game is ended, and representing the score. |
| As a  user I want to see the score go up upon hitting the mole | Mole is visible                       | High   | Successfully hitting a mole                  | Score increments by 1 and mole goes back into the hole       |
| As a user I want lives left to decrement by 1 upon hitting a bomb | Bomb is visible                       | Medium | Successfully hitting a bomb                  | Lives left decrements by 1 and bomb disappears.              |
| As a gamer I need to see the timer to game harder            | Game state = game                     | Medium | Pressing Start button on the top of the view | A timer will be visible at the bottom of the screen, displaying seconds left |
| As a user I want the game to be responsive and scale down to a mobile screen width | Open the game on  mobile screen width | Low    | Open the game on  mobile screen width        | The game sprites and background are scaled accordingly to the mobile mockup |

