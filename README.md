# Hex_Cards
Base repo for first round prototype of game

## Basics

   1. Start with a blank hex grid. 
   2. Each player controls one hex space. 
   3. Each player takes turns to play.
   4. Cards represent actions and objects
   5. Actions can be performed by the player or by objects (or the board?)
   6. Actions can be performed on the player himself, the opposing player, on objects, or on the board.
   7. Victory conditions between objects are determined by object-property rock/paper/scissors
   
### Loss conditions
* Player does not control any hex spaces and has no potential actions.
* Player forfeits.
* Player has no objects on the board and no objects in hand?


### Design principles
* All objects and action have one of seven attributes (think MtG)
  * a > b > c > d > e > f > g
    * a > b, d, f; b > c, e, g; etc.
    * does this result in sanity?
* 6x6 hex grid, flat bottom
* Start point 

* Avoid (player/object) hit points?
  * All outcomes are determined by either success/loss/no result
  
   
## Questions at first

* Start with 2P or nP? 
  * 2P would be probably simpler
  * Solving nP would be easier upfront and possibly require less refactoring
* Online? (Almost certainly?)
  *  Hotseat a possibility (focus on gameplay, not network coding)
*  Start point - set or decided?
* if -
two objects are different, one is destroyed based on the rps logic
two objects are the same, they either
occupy the space together and the tile doesn't change
or
are returned to previous space

## Prototype

* C# & Unity
* 6x6 grid
* objects are A/B/C (where A>B>C>A...)
* moves are simultaneous, turn based, resolution at end of turn.
* cards are 'place object' and 'move object'
  * place = .25, move = .25
* start point is static
* loss condition = no objects on board, no objects in hand
