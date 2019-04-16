---


---

<h1 id="drawing-shapes">Drawing Shapes</h1>
<p>In our first sketch we drew a square. There are commands to help you draw lots of shapes in Processing.</p>
<p>Each shape needs certain information to draw. Usually, the starting x and y coordinate (the top left corner of the screen is 0, 0), and the size of the object.</p>
<p>Copy the following program to see how some of the shapes work.</p>
<pre><code>void setup() {
    size(800, 600); // make a window 800px wide and 600px high
    background(255); // white background
    square(200, 300, 50); // square at x=200, y=300, 50px wide
    circle(100, 100, 30); // circle at x=100, y=100, 30 wide
    rect(400, 200, 30, 100); // rectange at x=400, y= 200, 30 wide, 100 high
    point(50, 50); // point at x=50, y=50
    line(20, 20, 600, 100); // line from x=20, y=20 to x=600, y=100
    ellipse(600, 400, 80, 50); // ellipse at x=600, y=400, 80 wide, 50 high
}
</code></pre>
<h3 id="adding-color">Adding Color</h3>
<p>Shapes can also have color. The color is controlled by r,g,b (red, green, blue) values from 0 to 255. You can make any color by mixing these three colors. Each number tells the computer how bright that color should be. Here are some examples.</p>
<pre><code>void setup() {
  // creates a window that is 800px wide and 600px high.
  size(800, 600);
  background(255); // Color the background white

  fill(51); // grey fill
  rect(400, 100, 50, 200);

  strokeWeight(10); // 10px thick outline
  fill(255, 0, 0); // red fill
  circle(100, 400, 50);

  strokeWeight(5); // 5px thick outline
  stroke(255, 0, 255); // purple outline
  fill(0, 255, 0); // green fill
  square(50, 100, 25);

  noStroke(); // no outline
  fill(0, 0, 255); // blue fill
  ellipse(500, 400, 80, 60);
}
</code></pre>
<p>Notice the all of the double slashes “<strong>//</strong>”. These create comments.</p>
<p>Comments are parts of the code with information for people, but they are ignored by the computer. This way you can write notes for yourself or for others to explain your code.</p>
<h3 id="things-to-try">Things To Try</h3>
<ol>
<li>Play around with different colors, each value can be between 0 and 255.</li>
<li>Try different <code>strokeWeight()</code> values, and try setting <code>noStroke()</code>.</li>
<li>Notice that once you set the value of the stroke, and fill any shapes you draw <strong>after</strong> those commands will have the same stroke and fill.</li>
</ol>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

