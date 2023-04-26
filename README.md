# Axy Snake Game
![Logo](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRneJ-ykE9L2KWZiZDcSODRWdYJN8gxET7Il1cgEF_Qz1bUQl-uSy6A6uP84077Ae8ezm3ChLo_GEQ&usqp=CAU&ec=48600113)

A clone of the most popular vintage Axy snake game which is mostly played in pc and mobile phones.

# Preview 

![snake_2](https://user-images.githubusercontent.com/113198704/234667400-5f2ca216-9ab2-426d-80b1-762b042a7f43.png)
![snake_4](https://user-images.githubusercontent.com/113198704/234667426-f22fe186-7385-4497-b873-8be035983f76.jpg)
![snake_3](https://user-images.githubusercontent.com/113198704/234667443-2bedc6c4-76b6-464e-a467-4a3a3469f4c0.png)
![snake_1](https://user-images.githubusercontent.com/113198704/234667496-41423abd-c68f-4bcc-93fa-e1419ec20bc6.png)







## Table of Contents

 - About
 - Getting Started
 - Deployment 
 
 - Design Approach
 - Built Using
 - Color reference
 

 - Acknowledgements


## About
Axy Snake game application is the replica of the most well known nostalgic Axy-snake game which is designed for the entertainment and general liteweight gaming purpose. This game totally depends upon the users D-pad directions controls through which the snake can imitate its move towards its food and thereby increasing the score along with its size.



## Getting Started
The Game begins at the run of the program, and snake starts its initial moment in it’s free direction. From there onwards, user can direct the snake towards its food which will pop at any certain place in the arena box. Using the D-pad or arrow keys, the user or gamer will direct the snake towards the red dot(can be known as Red apple).

When the snake touches the red apple, the apple will be eaten and the size of the snake will be increased by giving one point. 

 As soon as the previous apple eaten, new Red apple will be generated at another area and similarly snake can be directed towards that point for gaining the score. This process will be repeated and continued until the user can handle the snake without touching the borders of the arena or being the tail eaten by the snake itself.

## Deployment

This project is deployed into github by creating a new repository and following the below commands in the Vs code terminal.

```bash
 git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ManotejPatlolla/Example.git
git push -u origin main
```

## Design Approach
The game is designed by creating a layout of 600 x 600 in which the snake can run around the borders and eats the food. In color, snake is created in contrast with the food color( To display the variation).

Hence, score will also be shown at the top of the screen. Each time the apple eaten, the score will be increased by one. Therefore, larger the snake, higher the score.

Each and every dimension is coded until the perfect game play size is achieved. Foundation is created by mentioning the Public class GamePanel, where the Screen resolution(Width and height), Unit size(box per cm), Game units(Elements includes food) and the snake delay are mentioned.

In public class, appleX, appleY(axis for Apple) are initialized and char direction D is declared, so that snake will be moved towards down direction(Hit-free) after the program run. Along with them, some of the other methods are also initialized which serves the motions of the game.

Every action is performed by mentioning them in the GamePanel method which acts like a constructor. 

Background is set to Black color which makes the interface and elements to be in more contrast by using this.setBackground 

MyKeyAdaptor() holds the moments of the snake which can be achieved through the D-PAD.

## Methods for Play

### MyKeyAdapter(): 
Primary important method which is used to generate the moments for the snake using the D-pad. 

In-built methods like getKeyCode() and keyEvents makes the direction implementation very simple.

### move(): 
This method holds the moment of tha snake in all the directions. Swith case statement is used for creating the directional moving of the snake in all the directions.

### checkCollisions(): 
In checkCollisions(), the snake is programmed to end the game is the snake touches its body-parts or touches the boundaries of the box. Firstly, the for loop is used to declare whether the snake’s X and Y position hits the bodyparts, the game will be over. That is If , x[0] == x[i] or y[0] = y[i] the game running is false (game over). 

Here, i = bodyparts
Similarly, checkCollisons() deals with the directional aspects also.

### checkApple(): 
This code deals with the actions like popping the new apples (newApple()) at any places after the present apple is eaten, and also increases the snake size.

#### Actions performed in checkApple();
Bodyparts++ : increase the body parts. 

applesEaten++ : deals with the score. 

newApple() : generates the new apple at another place.

### gameover() :
Every game has an end. This game is coded to end when the user makes the snake to touch the boundaries of the box or makes itself eaten by touching its own body-parts.


## Built Using
 - [ Java ](https://en.wikipedia.org/wiki/Java_(programming_language)) - Programming language
  - [ Eclipse IDE ](https://eclipseide.org/) - Java platform environment

  ## Color Reference
All the colors used in this clone game are the shades of the below colors. Red and green are the base colors of this java game which makes the differntiation between food and moving element (Snake) easily.

| Color             | Hex                                                                |
| ----------------- | ------------------------------------------------------------------ |
|Red | ![#ff0000 ](https://via.placeholder.com/10/ff0000?text=+) #ff0000  |
| Yellow| ![#f7eb1e](https://via.placeholder.com/10/f7eb1e?text=+)#f7eb1e |
|Green | ![#25b681 ](https://via.placeholder.com/10/25b681?text=+) #25b681  |
| Grey | ![#181818](https://via.placeholder.com/10/181818?text=+)#181818 |





## FAQ

#### How can the snake will increase its length when it touches the apple?

Intially, ApplesEaten() and bodyparts() are declared in the program. A method call checkapple() which contains the above two methods when the snake touches the apple.

#### Will the snake cross its tail when touched?
No. The snake is programmed to stop and display Gameover as it has bitten its tail.


#### What is the main Objective to do this project?
To code a game logically using Oops concept.




## Acknowledgements
 - [Mozilla Webdocs](https://developer.mozilla.org/en-US/) (Oops fundamentals).

 - [Tech Gun](https://www.youtube.com/@TechGun) (Java fundamentals)

