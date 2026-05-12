# Javascript_games
The webiste I made at the end of Highschool, containing games i made using HTML, CSS and JavaScript. This was made before the rise of AI generative models like ChatGPT. 

All the files started as a blank .txt file, which i edited in notepad++. Compy-paste was used, but otherwise, every single line was writen by myself, without autocomplete or AI models. I also had to track down every error myself, looking through the code as well. HOwever, because of this, i knew the code very very well. Because its a locally run website, with no external dependancies, its does not 'save' progress reliably.  but does use local storage via the browser for high score tracking. 

Each game is based of the idea that there is a html table acting as the grid behind it all. this table will have a series of classes that can be applied to each table cell. these classes are added or removed by the javascript program, which decied when to do it off the logic  / state it contains. Buttons or keyboard presses are used to start the javscript processes. Because the table is a grid, an array of arrays is used (ie, 2D array) to store the current state of all the table cells. 

Where time delays or time-dependant games are involved, i had to use a built in javascript function that would run a given function after a delay. Hence, the function would simply call itself if no end condition is met and the games then heavily evolve around a 'tick'  based system, where all the calcuations are done and it upadte the system each time. A common workflow will be as follows:

    RunGame(){
      update_entites_locations()
      check_game_status()
      if game_status == over:
        end()
      else:
        runFunctionLater(RunGame, timedely)
    }
with a seperate function detecting keyboard interaction and updates the global state. 

The games that I have made, in order of creation are as follows:

Not-So-Flappy-Dot:
Its kinda like flayy bird, except a square tile and no gravity. basically a stnadard avoid the incoming objects  game.
However, this was my first one. So it was where i learned to get javascript to interact reliably with HTML, have a delay, get keyboard and mouse interactions and build a framework that i could use later. 
The majority of the frameworks built here become the basis (ie, copied and pasted) for the rest of the games, although edited for each one. 

Dot-man
My pac man replica. 


Minesweaper
I had heard of the idea of recursive functions from my dad. the decription i was given was "A function that can call itself". So, without looking it up, i had to find a use for this type, and find a way to impliment it. Although I didnt relise the time delay was one, Minesweaper made use of a much better example. 
The recursive  function here is used clear the tiles as the user clicks on them. In general, the user can click on a numbered tile or empty tile without anything going badly. If they click on a "mine", they loose. Numbered tiles do not clear any around them, but empty tiles should clear all the tiles around them until they uncover a numbered tile. because the ditribution of empty tiles is unknown and random, i had to use a recursive function here. Obviously i came across teh usual traps of infinite recursion, but eventaully, i got a working verion. This put me in a very good place later when got to university and were taught them for real. I had no problems with them then. 

When i first started making this game, i didnt really know how to play it, and nor was i very good. hence, the game over / win conditions where infrequently come by, and may still remain buggy

Tetris 
A remake of tetris. originally meant to play about with rotational matrices, i ended up just manually altering the shapes. Also orignally designed to have various other entites interaction with each other (ie, the shapes can knock another shape)

Snake:
Made in 6 hours when i should have been studying for a maths exam. Based of the respberry pi version of snake (ie, boring and simple). Maths exam later that week went well anyway. 

Wordle:
I made my version of wordle despite never looking at even the interface for the game. just based of the rules i heard people discussing about. Im quite terrible at the game, but i found i could easily do it if i turned of the line of code that made you have to  use real 5 letter words, and allowed any random 5 letters. 
 my JS code for this is only about 120 lines. plus ~2,500 lines of 5 letter english words.... 



Also, due to some high school banter, The website and games are designed deliberatly not to work when the browser is microsoft Edge. the detection code for this was taken from a stackOverflow. Should it detect edge from being used, the game stops. and usually error messages pop up to prevent you playing any further. 


