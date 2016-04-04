# Game Project Scope Study

## Required Readings

-   [Game Project](https://github.com/ga-wdi-boston/game-project)
-   [Game API](https://github.com/ga-wdi-boston/game-project-api)
-   [What is a User Story](http://searchsoftwarequality.techtarget.com/definition/user-story)

## Deliverables

After reading the `game-project` prompt and the `game-project-api` documentation
please do the following and be prepared to share and discuss on Monday morning.

Submit detailed answers to these in this file via a pull request.

-   A wireframe of what your game project will look like.
See Moqups link: <https://app.moqups.com/olliiviia/o9hwhjxk/view>

-   The data structure you plan to use.
  - How you will take the markup of the game board and represent it in JS

I will have the game board represented as an array object, with each square of the game being accesible via its index. I will then be able to change the value of each square with jquery when either player_x or player_o clicks on it. Values of the array items in the board can be either "x", "o", or "".

Other data structure considerations...
Per the Game Project API--
  * Users will be stored in the following format (JSON string):

  {
    "user": {
      "id" : 1,
      "email" : "example@example.com"
    }
  }

* Games will be stored as associated with each user, in the following format (JSON string):

{
  "games": [
    {
      "id" : 1,
      "cells" : ["", "", "", "", "", "", "", "", ""],
      "over": false,
      "player_x" : {
        "id": 1,
        "email": "example@example.com"
      },
      "player_o" : {
        "id": 2,
        "email": "another@another.com"
      }
    }
  ]
}

* User log in information will be stored as a javascript object on the front end each time a user logs in:

const app = {
  api: 'http://tic-tac-toe.wdibos.com',
  user: {
    id: 1,
    email: "example@example.com",
    password: "examplePassword",
    token: "tokenStringGoesHere"
  }
}

-   How you plan to approach this project.
I first plan to create the basic HTML structure and styling for the page with the sign up/log in forms, and the game board. I will then delve into the game logic of how to know when a game is complete, using JavaScript. Then I will use Jquery/Ajax to create interactivity on the site and link the front end to the API--first by connecting the user sign up/log in forms, and then the game play.

-   4-8 user stories for your game project.
*   As a user, I want to be able to have a log in account so that I can view my game hisory.
*   As a user, if my log in fails--I want to know if I entered an incorrect password or if the e-mail I entered is not associated with an account yet.
*   As a user, I want an interactive scoreboard that tells me how many games I've won against an opponent.
*   As a user, I want to be able to customize the token that I play with.
*   As a user, I want to be able to see my win/loss history and know if my record is imporoving over time.
*   As a user, I want to be able to view my opponents win/loss record so I know what I'm up against.
*   As a user, I want to be able to log out in the middle of a game, and be able to come back to the same game the next time I log in.

-   How you plan to keep your code moodular.
Similar to our in class projects, I will have seperate files for the html code, main js code, user interface js code, js code that interacts with the API, js code that listens for events on the page, etc.

-   What creative spin will you add to your project.
Hoping I can animate the chalk drawing of the X's, O's and winning lines/cat game. Maybe with sound effects? Want users to be able to customize their tokens and see game history stats--maybe with fun data viz with D3 js library. Maybe users can choose the color chalk they want to draw in.

-   How you will use version control to backup / track your project.
I will add and commit after every feature I want to add is complete. Maybe with different branches for html/javascript/css.

-   Do you plan to attempt any of the bonuses.
Really depends how much time I have. I would rather do a really good job on just the basic assignment versus a rush job on all of the bonuses. If I have time to start any of the bonuses I will, since that will be a good learning experience, but I won't add them to my final project unless I'm happy with the result.
