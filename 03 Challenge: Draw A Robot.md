---


---

<h1 id="challenge-draw-a-robot">03 Challenge: Draw A Robot</h1>
<p>In this challenge we will draw a Robot.</p>
<p>Copy this code carefully. Be sure to include all of the semicolons. You can stop after each command and run your sketch to see what each command draws.</p>
<pre><code>// Robot Code
void setup() {
    size(720, 480);
    strokeWeight(2);
    
    // Neck
    stroke(102);             
    line(266, 257, 266, 162);
    line(276, 257, 276, 162);
    line(286, 257, 286, 162);
    
    // Antennae
    line(276, 155, 246, 112);
    line(276, 155, 306, 56);
    line(276, 155, 342, 170);
    
    // Body
    noStroke();               
    fill(102);              
    ellipse(264, 377, 33, 33);
    fill(0);                 
    rect(219, 257, 90, 120);
    fill(102);              
    rect(219, 274, 90, 6);  
    
    // Head
    fill(0);                 
    circle(276, 155, 90);
    fill(255);               
    circle(288, 150, 28);
    fill(0);                
    circle(288, 150, 6);
    fill(153);             
    circle(263, 148, 10); 
    circle(296, 130, 8);
    circle(305, 162, 6);
}
</code></pre>
<h3 id="things-to-try">Things To Try</h3>
<ol>
<li>Color your robot. Make each part a color. You can use <code>fill()</code> to color the inside of the shapes and <code>stroke()</code> to color the outline of a shape, or <code>noStroke()</code> for no outline.</li>
<li>Add a comment with double slashes “<strong>//</strong>” after each color, to explain what color your code makes.</li>
</ol>
<p>Now that we have a robot, let’s learn how to animate it so we can make it move and do stuff!</p>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

