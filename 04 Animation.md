---


---

<h1 id="animation">Animation</h1>
<h3 id="animation-1">Animation</h3>
<p>The setup function will only run once. It basically draws the background of your project. If you want to make things change, you need a second function, the “draw” function. This will repeat over and over (every frame, something like 30 or 60 times a second). Here is an example.</p>
<pre><code>void setup() {
  // creates a window that is 800px wide and 600px high.
  size(800, 600);
  background(255); // Color the background white
}

void draw() {
  circle(mouseX, mouseY, 50);
}
</code></pre>
<p>This code draws a new circle every frame at the current position of your mouse.</p>
<h3 id="things-to-try">Things to Try</h3>
<ol>
<li>Move the “background” method from <strong>setup</strong> to <strong>draw</strong>. What happens?  Why?</li>
<li>Draw a line wherever you move your mouse with this code:<br>
<code>line (pmouseX, pmouseY, mouseX, mouseY)</code><br>
(Hint: pmouseX, and pmouseY stand for “previous mouse X” and “previous mouse Y”.)</li>
</ol>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

