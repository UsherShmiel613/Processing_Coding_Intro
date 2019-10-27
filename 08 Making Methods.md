<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>08 Making Methods</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h1 id="making-methods">08 Making Methods</h1>
<p>As we have seen from the previous sections, we can write simple instructions for the computer, and the computer will follow these instructions line-by-line. A computer will happily continue following these instructions for 10,000 lines.</p>
<p>However, as humans, we have trouble with long code. It become more complex, harder to understand, and harder to keep organized.</p>
<p>To make things simpler for us, it is good to group code together into logical chunks. These chunks can be easier to organize, and can make a program easier to understand. One way that we do this is by writing our own methods.</p>
<p>Creating our own functions allows us to organize our code into smaller chunks and treat complicated tasks as a single step.</p>
<p>We can also use predefined functions that Processing calls automatically do do things like perform animations and get user input.</p>
<h3 id="example">Example</h3>
<p>Here is a simple program for creating a ball, having it move across the screen, and bounce off the walls.</p>
<pre><code>int x;
int y;
int speed;

void setup() {
  x = 0;
  y = height/2;
  speed = 5;
  size(800, 600);
}

void draw() {
  background(0);
  fill(255, 0, 0);
  circle(x, y, 30);
  x = x + speed;
  
  if (x &gt; width || x &lt; 0) {
    speed = -speed;
  }
}
</code></pre>
<h3 id="wouldnt-it-be-nice-if...">Wouldn’t it be Nice If…</h3>
<p>Wouldn’t it be nice if our code could look like this:</p>
<pre><code>void draw() {
  background(0);
  drawBall();
  moveBall();
  bounceBall();
}
</code></pre>
<p>This is much easier to read and understand for us humans.</p>
<p>Well we can! We just need to make our own methods with these names. Here is what this program would look like with our code organized into methods.</p>
<pre><code>int y;
int speed;

void setup() {
  x = 0;
  y = height/2;
  speed = 5;
  size(800, 600);
}

void draw() {
  background(0);
  drawBall();
  moveBall();
  bounceBall();
}

void drawBall() {
  fill(255, 0, 0);
  circle(x, y, 30);
}

void moveBall() {
   x = x + speed;
}

void bounceBall() {
    if (x &gt; width || x &lt; 0) {
    speed = -speed;
  }
}
</code></pre>
<h3 id="how-to-make-a-method">How To Make A Method</h3>
<p>To make a method we need 4 things:</p>
<ol>
<li>The “return type”—the expected <strong>output</strong>—of the method.</li>
<li>The name of the method.</li>
<li>Parenthesis, with a list of any parameters—the expected <strong>input</strong>—for the method</li>
<li>Curly braces containing the instructions—the <strong>process</strong>—of the method</li>
</ol>
<p>So basically a method is saying, “I’ll give you this, if you give me that, and this is how I’ll do it.”</p>
<h3 id="method-output-understanding-return-types">Method Output: Understanding Return Types</h3>
<p>When the computer is finished with a method, sometimes it gives you a value back. Other times, it doesn’t give you anything back.</p>
<p>For example, if you ask me to beat an egg to use in a cake, I will give you a bowl of beaten egg back. If you ask me to eat the cake, I’m not giving you anything back, because there’s nothing left.</p>
<p>Similarly, methods that draw a circle, or print something to the screen give nothing back, so their <strong>return type</strong> is <strong>void</strong>, which means empty.</p>
<p>A method that adds numbers, or calculates an average will give you back a number (<strong>int</strong> or <strong>float</strong>). A method that requests a user to input their name, will return a <strong>String</strong>. A method that checks if a game is over will return a <strong>boolean</strong> (true or false).</p>
<h3 id="method-examples">Method Examples</h3>
<p>This method draws a red circle. It returns nothing (<strong>void</strong>).</p>
<pre><code>void drawRedCircle(float circleX, float circleY, float circleDiameter){
  fill(255, 0, 0);
  circle(circleX, circleY, circleDiameter);
}
</code></pre>
<p>This method gives you the average of two numbers, and returns a number (<strong>float</strong>).</p>
<pre><code>float average(float num1, float num2) {
  float answer = (num1 + num2) / 2;
  return answer;
}

float myAverage = average(15, 35); 
</code></pre>
<p>This method tells you if a game is over.</p>
<pre><code>boolean gameOver() {
	if (points &lt;= 0) {
    	return true;
	} else {
		return false;
	}
}
</code></pre>
<h3 id="method-input-understanding-parameters">Method Input: Understanding Parameters</h3>
<p>(Example from <a href="https://happycoding.io/tutorials/processing/creating-functions">https://happycoding.io/tutorials/processing/creating-functions</a> )<br>
Just like we can get values back from our methods, often we need to give our methods information. We already saw examples of this when drawing and coloring shapes. For example, we gave values to the <code>circle()</code> method to tell it where and how big to draw our circle.</p>
<p>When we create our own methods, we get to decide what information our method needs to do its job. Let’s say we wanted to draw a target, we could make a method like this:</p>
<pre><code>void drawTarget(float targetX, float targetY, float targetSize) {

  fill(255, 0, 0);
  circle(targetX, targetY, targetSize);

  fill(255, 255, 255);
  circle(targetX, targetY, targetSize*.75);

  fill(255, 0, 0);
  circle(targetX, targetY, targetSize/2);
}
</code></pre>
<p>Now, we can use this method over and over, just like the methods that are built into Processing.</p>
<pre><code>void setup() {
  size(400, 400);
}

void draw() {
  drawTarget(100, 100, 200);
  drawTarget(300, 100, 100);
  drawTarget(100, 300, 150);
  drawTarget(300, 300, 175);
}

void drawTarget(float targetX, float targetY, float targetSize) {
  fill(255, 0, 0);
  circle(targetX, targetY, targetSize);
  fill(255, 255, 255);
  circle(targetX, targetY, targetSize*.75);
  fill(255, 0, 0);
  circle(targetX, targetY, targetSize/2);
}
</code></pre>
<p>We could also draw a target that follows the mouse:</p>
<pre><code>void draw() {
  background(200);
  drawTarget(mouseX, mouseY, 100);
}
</code></pre>
<p>Or we could fill the screen up with random targets:</p>
<pre><code>void draw() {
  drawTarget(random(0, width), random(0, height), random(25, 100));
}
</code></pre>
<h3 id="things-to-try">Things To Try</h3>
<ul>
<li>Create a  <code>drawHouse()</code>  function that draws a house. Take in parameters for the house location, size, color, etc.</li>
<li>Create a  <code>drawBlock()</code>  function that draws 4 houses. Take in parameters for the block location, size, color, etc. Don’t write code that draws 4 houses! Instead, call the  <code>drawHouse()</code>  function 4 different times with different parameters.</li>
<li>Create a  <code>drawNeighborhood()</code>  function that draws 9 blocks. Take in parameters for the neighborhood location, size, color, etc. Call the  <code>drawBlock()</code>  function to draw the blocks.</li>
<li>Create a  <code>drawCity()</code>  function that fills the window with neighborhoods.</li>
</ul>
</div>
</body>

</html>
