---


---

<h1 id="some-code-to-try">07 Some Code To Try</h1>
<p>It’s best to learn by doing. So, before learning more advanced coding concepts, let’s try some code that uses these features.</p>
<h4 id="growing-circles">Growing Circles</h4>
<pre><code>int circleSize = 0;

void setup() {
  size(640, 360);
  background(255);
  noStroke();
  fill(0);
}

void draw() {
  // Draw only when mouse is pressed
  if (mousePressed == true) {
    circleSize += 5; // adds 5 to circleSize
    circle(mouseX, mouseY, ballSize);
   } else {
    circleSize = 0; // resets the circleSize when you stop pressing the mouse
   }
}
</code></pre>
<h4 id="bouncing-off-walls">Bouncing Off Walls</h4>
<pre><code>int y = 300;
int w = 50;
int speed = 5;

void setup() {
  size(800, 600);
}

void draw() {
  background(0);

  circle(x, y, w);
  x += speed;

  if (x &gt; width || x &lt; 0) {
    speed = -speed;
  }
}
</code></pre>
<h4 id="bouncing-around">Bouncing Around</h4>
<pre><code>int radius = 60;        // Width of the circle
float xpos, ypos;    // Starting position of shape    

float xspeed = 2.8;  // Speed of the shape
float yspeed = 2.2;  // Speed of the shape

int xdirection = 1;  // Left or Right
int ydirection = 1;  // Top to Bottom

void setup() 
{
  size(640, 360);
  noStroke();
  // Set the starting position of the shape
  xpos = width/2;
  ypos = height/2;
}

void draw() 
{
  background(102);
  
  // Update the position of the shape
  xpos = xpos + ( xspeed * xdirection );
  ypos = ypos + ( yspeed * ydirection );
  
  // Test to see if the shape exceeds the boundaries of the screen
  // If it does, reverse its direction by multiplying by -1
  if (xpos &gt; width-radius || xpos &lt; radius) {
    xdirection *= -1;
  }
  if (ypos &gt; height-radius || ypos &lt; radius) {
    ydirection *= -1;
  }

  // Draw the shape
  circle(xpos, ypos, radius*2);
}
</code></pre>
<h4 id="repeating-lines">Repeating Lines</h4>
<pre><code>void setup() {
  size(800, 600);
  background(255);
  for (int lineX = 25; lineX &lt;= width; lineX += 25) {
    line(lineX, 0, lineX, height);
  }
}
</code></pre>
<h4 id="a-chess-board">A Chess Board</h4>
<pre><code>int gridSize = 50;

void setup() {
  size(400, 400);
  background(255);
  for (int h = 0; h &lt; height; h += gridSize) {
    for (int w = 0; w &lt; width; w += gridSize) {
      if ((h+w) % 20 == 0) {
        fill(255);
      } else {
        fill(0);
      }
      noStroke();
      square(w, h, gridSize);
    }
  }
}
</code></pre>
<h3 id="things-to-try">Things to Try</h3>
<ol>
<li>Copy these codes and try changing the values. What happens?</li>
<li>If you don’t understand anything in the code just ask!</li>
<li>Add comments to explain what you think each part of the code does.</li>
</ol>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

