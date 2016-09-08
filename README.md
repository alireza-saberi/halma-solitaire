# [Halma Solitaire](https://en.wikipedia.org/wiki/Halma)
It is a traditional board game that can be played indidiuallly or in group 

![image](https://upload.wikimedia.org/wikipedia/commons/7/7a/Halma4.svg)

Here, I code the solitaire version, beased on that I saw in the [Dive into HTML5](http://diveintohtml5.info/canvas.html) book.
Halma with 9 pieces on a 9 × 9 board. In the beginning of the game, the pieces form a 3 × 3 square in the bottom-left corner of the board. The object of the game is to move all the pieces so they form a 3 × 3 square in the upper-right corner of the board, in the least number of moves.

There are two types of legal moves in Halma:

- Take a piece and move it to any adjacent empty square. An “empty” square is one that does not currently have a piece in it. An “adjacent” square is immediately north, south, east, west, northwest, northeast, southwest, or southeast of the piece’s current position. (The board does not wrap around from one side to the other. If a piece is in the left-most column, it can not move west, northwest, or southwest. If a piece is in the bottom-most row, it can not move south, southeast, or southwest.)
- Take a piece and hop over an adjacent piece, and possibly repeat. That is, if you hop over an adjacent piece, then hop over another piece adjacent to your new position, that counts as a single move. In fact, any number of hops still counts as a single move. (Since the goal is to minimize the total number of moves, doing well in Halma involves constructing, and then using, long chains of staggered pieces so that other pieces can hop over them in long sequences.)

General rules to make games with `canvas`:

- Add an event listener: for click or keypress: `addEventListener()`
- Get the cursor position on the canvas: To do so. you have the position of the canvas in the document and it should be changed based on `offsetTop` and `offsetLeft` of the canvas
Whew! Mouse events are tough. But you can use the same logic (in fact, this exact code) in all of your own canvas-based applications. Remember: mouse click → document-relative coordinates → canvas-relative coordinates → application-specific code.
-  Clear and redraw the board in its entirety every time anything changes within the game.
