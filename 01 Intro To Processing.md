---


---

<h1 id="getting-started-with-processing">01 Getting Started with Processing</h1>
<p>Processing is a simple software that uses Java to make it easy to code graphics and animation, or even simple games.</p>
<p>To get started you need to download Processing from <a href="https://processing.org/">Processing.org</a>. Processing comes as a zip file. Save this somewhere convenient, and unzip the folder.</p>
<h3 id="running-processing">Running Processing</h3>
<p>Click on the processing application icon, and a “sketch” window will open. You can enter you code here.</p>
<p>To begin using processing you need a “setup” method. This tells the computer how to setup your project. It will run these instructions once at the beginning of your program.</p>
<pre><code>void setup() {
  size(800, 600);
}
</code></pre>
<p>Everything between the two curly braces “{  }” is one list of instructions. Each instruction needs to end with a semicolon " ; ". This is like a period for the computer—it tells the machine that one idea is finished.</p>
<p>So far our instructions don’t do much.</p>
<p>The single command we entered will create a grey window that is 800 pixels wide and 600 pixels high.</p>
<p>Let’s change the background color to black. Add the following instruction: <code>background(0);</code> on the next line. (And don’t forger your semicolons, or the program won’t run!)</p>
<pre><code>void setup() {
  size(800, 600);
  background(0);
}
</code></pre>
<p>Great! Now we have a black window.</p>
<p>The <code>background()</code> command takes a number from 0 to 255. 0 is black, 255 is white, and everything in between are different shades of grey. You can try a few numbers and see what happens. (We can also add color, but we’ll learn about that soon.)</p>
<p>Let’s draw a square on our sketch. To do this we use the command <code>square()</code>. For this command to work, we need to give it three numbers, the <strong>“x”</strong> location, the <strong>“y”</strong> location, and the size of the square in pixels.</p>
<p>The <strong>x</strong> location sets how many pixels from the left to draw the square. It can be any value from 0 to the width of the screen (which in our case is 800).</p>
<p>The <strong>y</strong> location sets how many pixels from the top of the screen to draw the square. It can be any value from 0 to the height of the screen (which in our case is 600).</p>
<p>Let’s draw a square at x = 200, and y = 300, with a size of 50 pixels. That will look like this <code>square(200, 300, 50);</code> .</p>
<pre><code>void setup() {
  size(800, 600);
  background(0);
  square(200, 300, 50);
}
</code></pre>
<p>Super! Now you drew your first Processing sketch. It may not be much, but this is a great start.</p>
<p>Processing has tons of commands that we can use to draw and animate our sketch, so there is lots to learn. Each new tool we learn will let us make our sketches more complex and more fun!</p>
<h3 id="things-to-try">Things To Try</h3>
<ol>
<li>Try changing the size of the sketch window.</li>
<li>Try changing the background color (from 0 to 255).</li>
<li>Try changing the position and size of the square.</li>
<li>What happens if you make the square’s position off the screen?</li>
</ol>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

