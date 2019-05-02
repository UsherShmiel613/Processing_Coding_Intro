---


---

<h1 id="using-variables">Using Variables</h1>
<ul>
<li><strong>Variables</strong> tell the computer to <em>remember</em> something.</li>
<li><strong>Variables</strong> can change (vary).</li>
<li><strong>Variables</strong> are like boxes or containers to hold things.</li>
<li>There are different size boxes to hold different things.</li>
<li>Variable names are usually written in camelCase</li>
</ul>
<p>Try these code snippets to see how variables work.</p>
<pre><code>void setup() {
  size(800, 600); 
  background(200); 
  circle(400, 300, 200);
  // This draws a circle in the middle of the screen
}
</code></pre>
<p>What if I want to change my screen size? I’ll need to change my circle’s position too.</p>
<p>Now try this:</p>
<pre><code>void setup() {
  size(800, 600); 
  background(200); 
  circle(width/2, height/2, 200); // "width divided by 2", "height divided by 2"
  // This draws a circle in the middle of the screen
}
</code></pre>
<p>This does the same thing, but now my code will automatically move the circle to the middle if I change my screen size.</p>
<h3 id="things-to-try">Things To Try</h3>
<ol>
<li>Change the screen size a few times and see how the circles stays centered.</li>
</ol>
<h4 id="animation-with-variables">Animation with Variables</h4>
<p>Variables let us animate our sketches. Try this code.</p>
<pre><code>int x = 1; // create an "integer" variable named "x" and set its value to "1"

void setup() {
  size(800, 600);
}

void draw() {
  background(200);
  circle(x, 300, 30); // draw the circle at position x
  x = x + 1; // increase x by 1 each loop
}
</code></pre>
<p><strong>Congratulations!</strong> You just created your first variable.</p>
<h3 id="things-to-try-1">Things To Try</h3>
<ol>
<li>Change the ball’s speed.</li>
<li>Make the ball go from right to left.</li>
<li>Can you make the ball fall from the top down, instead of moving from left to right?</li>
</ol>
<h4 id="pre-made-variables">Pre-Made Variables</h4>
<p>Some variables come pre-made in Processing. You can just use these.</p>
<ul>
<li>mouseX = the “x” position of your mouse</li>
<li>mouseY = the “y” position of your mouse</li>
<li>width = whatever you set as the screen width</li>
<li>height  = whatever you set as the screen height</li>
</ul>
<h4 id="making-your-own-variables">Making Your Own Variables</h4>
<p>You can also make your own <strong>variables</strong>. Each variable creates a “box” in the computer’s memory to hold some information. To create a <strong>variable</strong> you need to tell the computer three things.</p>
<ol>
<li>What kind of box you want to create (will it hold numbers, words, etc.)</li>
<li>A name for your box</li>
<li>Information (a value) to put in the box</li>
</ol>
<p>There are four basic kinds of boxes you can make</p>
<ol>
<li>Whole numbers (integers), like 1, 42, or -15</li>
<li>Decimal numbers (floating point), like 3.14, 15.99, or -100.4</li>
<li>Words (a String of characters), like “hello”, or “this is fun”</li>
<li>True/False (called a boolean), like true, or false</li>
</ol>
<p>For now, we’ll just use the first kind of box—Integers.</p>
<p>Try this code:</p>
<pre><code>int x = 0; // "x" position of the cirlce
int y = 0; // "y" position of the cirlce
int w = 10; // "w" is for the width of our circle

void setup() {
  size(800, 600);
}

void draw() {
  background(200);
  circle(x, y, w); // draw the circle at position x
  x = x + 1; // increase x by 1 each loop
  y = y + 1; // increase y by 1 each loop
}
</code></pre>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

