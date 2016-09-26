# html, css, dom manipulation
 You should create simple html game ([demo](https://koalacoders.github.io/jump/))

 Your code structure should be like this:
 ```js
 class Player { }
 class Barrier { }
 class Game { }
 ```

 ## Player
 ```js
 class Player {

   constructor(game) {
    /*
      Add event listener for keydown
    */
   }

   moveLeft() { }

   moveRight() { }

   jump() { }

   render() { /* Should append html to game.holder */ }

 }
 ```

 ## Barrier
 ```js
 class Barrier {

   constructor(game) {
     /*
      Add interval which
     */
   }

   move() {  }

   render() {
   /*
    Slould append html with position out of screen to game.holder
   */
   }

 }
 ```

## Game
```js
class Game {

  apdateInterval: number

  holder: htmlElement

  bariers: Array of Barrier instances

  constructor() {
    /*
      1. Create player
      2. Run bariers generator
    */
  }

  bariersFactory() {
    /*
      Should create interval which will produce new barriers
    */
  }

  check(barier) {  /* Should check does player touched barrier */ }

  render() { /* Should render general game field */ }

  renderGameOver() { /* Should render screen when game failed */ }

}
```
