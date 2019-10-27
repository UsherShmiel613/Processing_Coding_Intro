<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>10 Repeating Stuff with Loops</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h1 id="repeating-stuff-with-loops">10 Repeating Stuff with Loops</h1>
<p>Sometimes we need to repeat something over and over. We could just write the same or similar code a bunch of times. This (could) get(s) annoying to type and hard to change.</p>
<p>Instead, we can tell the computer to repeat something for us!</p>
<p>For example, if we want to make draw 500 stars in random locations, we don’t need 500+ lines of code. Instead, this code will generate 500 stars at random locations, with a random size up to 3 pixels.</p>
<pre><code>void setup() {
  size(600, 600);
  background(0);
  stroke(255);
  for (int stars = 0; stars &lt; 500; stars++) {
    strokeWeight(random(3));
    point(random(width), random(height));
  }
}
</code></pre>
<h3 id="how-a-for-loop-works">How a For Loop Works</h3>
<p>A <strong>For Loop</strong> is a special method that repeats its code as many times as we tell it to. To create a for loop use the <strong>for</strong> keyword. In the parenthesis we give three values as input:</p>
<ul>
<li>Make a variable to keep count of how many times you loop through your code. Often this variable is called <strong>i</strong> for “index”, but you can use whatever name you like.</li>
<li>Write a condition for when to stop the loop. The loop will continue as long as this condition is <strong>true</strong>, and will stop as soon as this condition is <strong>false</strong>. The simplest example is when your index is higher than a certain value. So <code>index &lt; 10</code> will only run until the value of index is 10 or higher.</li>
<li>Change the value of your index after the code runs. Usually this is simply adding 1 to the index, which is usually written as <strong>i++</strong>. Sometimes, you may want to use a different operation here.</li>
</ul>
<p>For example, this simple for loop will print the value of <strong>i</strong> to the console 10 times, from 0 to 9.</p>
<pre><code>void setup() {
  for (int i = 0; i &lt; 10; i++) {
    println("i is now: " + i);
  }
}
</code></pre>
<h3 id="make-a-game-board">Make A Game Board</h3>
<p>We can use loops to draw a game board—for example, if we want an 8 x 8 board for chess or checkers. This code will draw 8 lines.</p>
<pre><code>void setup() {
  size(600, 600);
  background(255);
  strokeWeight(4);
  for (int lineX = 0; lineX &lt; width; lineX = lineX + width/8) {
    line(lineX, 0, lineX, height);
  }
}
</code></pre>
<br>
<p><img src="https://lh3.googleusercontent.com/861STk3IU6aaaXzmwAl_S39uo5CrG-d02WoEtAMw2haeOHu9prJx2fBQW1P0qwCEbmSEKyuTn2s" alt="Chess Board Step 1" title="Chess Board Step 1"></p>
<p>We don’t need that first line, so we can start our index variable at a different value. I will make the grid size a variable and use that in our loop.</p>
<pre><code>void setup() {
  size(600, 600);
  background(255);
  strokeWeight(4);
  
  int gridSize = width/8;
  for (int lineX = gridSize; lineX &lt; width; lineX = lineX + gridSize) {
    line(lineX, 0, lineX, height);
  }
}
</code></pre>
<p>Now we need to add the horizontal lines. The spacing for the <strong>x</strong> and <strong>y</strong> position of the lines is the same—the gridSize, so we can use the same loop to make both sets of lines. I will rename the variable from lineX to lineSpace.</p>
<pre><code>void setup() {
  size(600, 600);
  background(255);
  strokeWeight(4);
  
  int gridSize = width/8;
  for (int lineSpace = gridSize; lineSpace &lt; width; lineSpace = lineSpace + gridSize) {
    line(lineSpace, 0, lineSpace, height);
    line(0, lineSpace, width, lineSpace);
  }
}
</code></pre>
<p><img src="https://lh3.googleusercontent.com/twcNaqjsj2Z5Bro5AGcKe-XVN5I6eYhN_eaJr1b3cTJyQBQ7LdOSINPsd8IYRLcYV3__1W3jMOw" alt="Chess Board Step 2" title="Chess Board Step 2"></p>
<p>This code is also reusable! If we change the gridSize to width/3 it will make a TicTacToe board.</p>
<h3 id="a-chess-board-with-squares">A Chess Board with Squares</h3>
<p>We can use a similar process to make a black and white chess board. But for this we need a loop inside of a loop. This is called a <strong>nested loop</strong>.</p>
<pre><code>int gridSize = 50;
int margin = 20;
int boardSize = gridSize * 8;

void setup() {
  size (440, 440);
  background (0);
  
  // Makes a White border around the board
  strokeWeight (3);
  stroke (255);
  noFill();
  square(margin, margin, boardSize);
  
  // Draw a white square for every other grid position
  noStroke();
  // The first loop goes accross a row from left to right
  for (int x=margin; x&lt;boardSize; x+=gridSize*2) {
  // The second loop goes down a column from top to bottom  
    for (int y=margin; y&lt;boardSize; y+=gridSize*2) {
      fill (255);
      square(x, y, gridSize);
      square(x+gridSize, y+gridSize, gridSize);
    }
  }
}
</code></pre>
<p>Nested loops are confusing, so you can use methods to make things easier to understand. The method names take the place of comments, making our code more organized and easier to understand!</p>
<pre><code>int gridSize = 50;
int margin = 20;
int boardSize = gridSize * 8;

void setup() {
  size (440, 440);
  background (0);
  
  // Makes a White border around the board
  strokeWeight (3);
  stroke (255);
  noFill();
  square(margin, margin, boardSize);
 
  for (int y=margin; y&lt;boardSize; y+=gridSize*2) {
    drawBoardRow(y);
  }
}

void drawBoardRow(int y) {
  for (int x=margin; x&lt;boardSize; x+=gridSize*2) {
    noStroke();
    fill (255);
    square(x, y, gridSize);
    square(x+gridSize, y+gridSize, gridSize);
  }
}
</code></pre>
<h3 id="things-to-try">Things To Try</h3>
<ul>
<li>Write a program that makes 10 circles across the screen.</li>
<li>Write a program that makes 10 rows of 10 circles.</li>
<li>Write a program that draws a horizontal gradient. Hint: draw  <code>width</code>  lines, and make each one a darker shade of gray.</li>
<li>Write a program that makes every pixel in the window a different random color.</li>
</ul>
</div>
</body>

</html>
