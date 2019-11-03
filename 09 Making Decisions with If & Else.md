<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>09 Making Decisions with If &amp; Else</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h1 id="making-decisions-with-if-and-else">09 Making Decisions with If and Else</h1>
<p>We already saw some examples of if statements in our <strong>Bouncing</strong> examples. Now let’s learn more about how these work.</p>
<p><strong>If / Else Statements</strong> are used to make decisions, which is one of the <strong>5 Kinds of Code</strong></p>
<ol>
<li>Do Stuff</li>
<li>Remember Stuff</li>
<li>Repeat Stuff</li>
<li><strong>Decide Stuff</strong></li>
<li>Organize Stuff</li>
</ol>
<p>Anytime we want the computer to behave a certain way sometimes, and behave differently the rest of the time, we need to use <strong>decisions</strong>.</p>
<h3 id="boolean-logic">Boolean Logic</h3>
<p>Computers use very simple logic to make decisions. Everything is either <strong>true</strong> or <strong>false</strong>.</p>
<p>You can ask the computer three kinds of True or False questions:</p>
<ul>
<li>Greater than ( &gt; )</li>
<li>Less than ( &lt; )</li>
<li>Equal to ( == )</li>
</ul>
<h3 id="bar--bat-mitzvah-card">Bar / Bat Mitzvah Card</h3>
<pre><code>String name = "Chaim";
int age = 13;
boolean boy = true;
String eventType = " ";

void setup() {
  size(800, 600);
  background(255);

  // if boy AND age EQUALS 13
  if (boy &amp;&amp; age == 13) {
    eventType = "Bar Mitzvah";
  }
  // else if NOT boy AND age EQUALS 12
  else if (!boy &amp;&amp; age == 12) {
    eventType = "Bat Mitzvah";
  }
  // for all other cases
  else {
    eventType = "Birthday";
  }
  
  drawCard();
  addMessage();

}

void drawCard() {
  fill(242, 239, 225);
  rect(200, 50, 400, 500);
  fill(0);
  textAlign(CENTER);
  textSize(32);
  text("Mazal Tov!", width/2, 100);
}

void addMessage() {
  fill(0);
  textAlign(CENTER);
  textSize(32);
  text("Join us for the", width/2, 250);
  text(eventType + " of", width/2, 300);
  text(name, width/2, 350);
}
</code></pre>
<h3 id="things-to-try">Things To Try</h3>
<ol>
<li>Change the name, age, and gender variables. Can you get the card to say “Bat Mitzvah”? Can you get it to say “birthday”?</li>
<li>Make the card background change color depending if it's for a boy or a girl.</li>
</ol>
<h3 id="mouse-on-left">Mouse On Left</h3>
<p>Let’s start by building a program to detect <strong>if</strong> the mouse if over a certain part of the screen.</p>
<p>In our case, let’s start by drawing a screen with a line down the center. The drawing could be in setup or in draw, but I’ll put it in draw in case we want to add more elements later.</p>
<pre><code>void setup() {
  size(600, 600);
}

void draw() {
  background(0);
  stroke(255);
  line(width/2, 0, width/2, height);
}
</code></pre>
<p>Great! Now let’s add some detection. If the mouse is on the left side, make the screen red. Otherwise, keep it black. To do this, we need an <strong>if statement</strong> to check the <strong>mouseX</strong> variable.</p>
<pre><code>void setup() {
  size(600, 600);
}

void draw() {
      
  if (mouseX &lt; width/2) {
    background(255, 0, 0); // red
  } else {
    background(0); // black
  }
  
  stroke(255); // white line
  line(width/2, 0, width/2, height);
}
</code></pre>
<p>Notice that we added the <strong>if statement</strong> <em>before</em> drawing the line. Otherwise, the line would be covered by the background.</p>
<h3 id="things-to-try-1">Things to Try</h3>
<ol>
<li>Draw a horizontal line halfway up the screen, so that the screen is divided into four equal parts.</li>
<li>Add to the <strong>if statement</strong> so that the screen only turns red if the mouse is over the upper left quadrant, but remains black for the other three.</li>
</ol>
<h2 id="challenge-yourself">Challenge Yourself!</h2>
<p>Sharpen your coding skills by completing these missions!</p>
<h3 id="missions-one-colored-quadrants">Missions One: Colored Quadrants</h3>
<p>Modify your code so that the background changes to a different color for each of the four quadrants (such as red, blue, green, and yellow).</p>
<h3 id="mission-two-smaller-targets">Mission Two: Smaller Targets</h3>
<p>Modify your code to have a square near the middle of the screen. Change the background color only when the mouse is over the square.</p>
<h3 id="mission-three-refactor">Mission Three: Refactor</h3>
<p>Let’s refactor our code! Make your mouse detection code into its own method called mouseOver(). Have this method take an x, y, width, and height and return true or false, so that your draw method looks like this:</p>
<pre><code>void draw() {
	if (mouseOver(x, y, w, h)) {
    	background(255, 0, 0);
    } else {
    	background(0);
    }
}
</code></pre>
<p>After this method is complete, you will have something that you can use over and over for all of the buttons you create in your projects!</p>
</div>
</body>

</html>
