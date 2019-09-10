<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>How Computers Work</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h1 id="how-computers-work">How Computers Work</h1>
<p>Before diving into making websites, it is helpful to have a little understanding of how all of this technology works. We won’t spend too much time on this, but I will link to a bunch of great resources. I highly recommend that you take the time to go through as much of these as you can. The more you understand about these technologies, the better you will be at wielding them.</p>
<h3 id="its-not-magic">Its Not Magic</h3>
<blockquote>
<p>Any sufficiently advanced technology is indistinguishable from magic.<br>
— Arthur C. Clarke</p>
</blockquote>
<p>Computers have become so embedded in our lives that we hardly need give them a second thought. They make many miracles possible—instantaneous communication, immediate access to vast stores of information, and immersive multimedia. All of this can create the impression that computers are magic black boxes possessing a mind of their own.</p>
<p>Yet, the truth is that computers are really just tools, doing very simple tasks. The magical complexity that we see comes from performing many of these simple task very quickly. Still, we need to learn to think about computers just like any other tool.</p>
<p><em>Technically, a computer could be purely mechanical, with no electronic parts—electronics are just way more efficient, because they are fast and small.</em></p>
<p><em>For example, checkout how a simple computer was built from dominoes.</em></p>
<ul>
<li><a href="https://youtu.be/lNuPy-r1GuQ">Domino Addition</a></li>
<li><a href="https://youtu.be/OpLU__bhu2w">10,000 Domino Computer</a></li>
</ul>
<p><em>For more about how computers work check out the amazing series <strong>Crash Course Computer Science</strong>. (These are free AP levels courses.) It will give you an overview of what a computer does at the most basic level, and how many simple components join to create the complex machines we know and love.</em></p>
<ul>
<li><a href="https://www.youtube.com/watch?v=tpIctyqH29Q&amp;list=PLME-KWdxI8dcaHSzzRsNuOLXtM2Ep_C7a">Crash Course Computer Science YouTube Playlist</a></li>
<li><a href="https://thecrashcourse.com/courses/computerscience?page=2">Crash Course Website</a></li>
</ul>
<h3 id="tool-time">Tool Time</h3>
<p>Let’s stop for a moment and think about what tools do. For example, a knife, a toaster, and a blender are all pretty simple tools.</p>
<p>Each tool makes a certain task easier or more efficient.</p>
<ul>
<li>A knife makes it easier to cut things, instead of ripping them apart with our bare hands.</li>
<li>A toaster makes toast quickly and even pops up when the toast is done so it doesn’t get burnt.</li>
<li>A blender mashes, mixes, and purees foods.</li>
</ul>
<p>These tools are not the only way to get these jobs done, but they are a very efficient way.</p>
<h3 id="the-ins-and-outs">The Ins and Outs</h3>
<p>One way to think about tools is a three step process:</p>
<ol>
<li>One or more items (ingredients or elements) go into the process.</li>
<li>The tool changes the items in some way (it processes them).</li>
<li>One or more changed items emerge.</li>
</ol>
<p>Let’s go through each of these tools and identify each stage. This may bea simple exercise, but it will lay the foundation for thinking about everything else in computing and programming.</p>
<h4 id="a-knife">A Knife</h4>
<ol>
<li><strong>What goes in?</strong> An apple and force applied by our hand.</li>
<li><strong>What is the process?</strong> The sharp blade of the knife converts the force of our hand into an efficient splitting force, cutting the apple in half.</li>
<li><strong>What comes out?</strong> A nicely sliced apple.</li>
</ol>
<h4 id="a-toaster">A Toaster</h4>
<ol>
<li><strong>What goes in?</strong> A slice of bread and electricity.</li>
<li><strong>What is the process?</strong> The heating element in the toaster converts the electrical energy into heat at the right intensity for toasting bread.</li>
<li><strong>What comes out?</strong> Toast.</li>
</ol>
<h4 id="a-blender">A Blender</h4>
<ol>
<li><strong>What goes in?</strong> Kale, broccoli, almond milk, and electricity.</li>
<li><strong>What is the process?</strong> The blender’s motor coverts electrical energy into a strong rotational force, which is transferred to the blades, which puree the ingredients.</li>
<li><strong>What comes out?</strong> A health smoothie that looked good in the picture, but no one wants to drink.</li>
</ol>
<h4 id="with-great-power-comes...">With Great Power Comes…</h4>
<p>The examples we gave so far are all pretty simple tools. But what about something bigger and more complicated like a car?</p>
<p>On the one hand, its still pretty simple. We put in gas, force on the gas petal, and force on the steering wheel. The car converts the gas into motion of the wheels in the direction we point the steering wheel. We get from point A to point B.</p>
<p>Yet, under the hood, there is a lot going on to make this all happen. There are dozens of smaller tools that are working together to make the car work. But as long as these smaller parts are all bundled together and working properly, we can forget about them and just drive.</p>
<p>The bundling of simpler tools to make more powerful complex tools is one of the fundamentals of good, user-friendly technology. When we use a car or a phone, we don’t need to know how all of the part work. All we need to know is what to put in, and we’ll get what we need coming out.</p>
<p><em>The bundling of simpler tools to make more powerful tools in a way that the user doesn’t need to think about the smaller parts is called <strong>Abstraction.</strong></em></p>
<h3 id="whats-the-point">What’s The Point?</h3>
<p>These simple examples demonstrate something fundamental to all tools—and remember a computer is just another tool. Everything that happen in computing is really just <strong>input</strong>, a <strong>process</strong>, and <strong>output</strong>.</p>
<p>Sure computers are very complex under the hood, but fundamentally, and at every level, the computer is just taking input, processing it, and giving output.</p>
<p>If you really want to get technical, all a computer really does is add binary numbers. And addition is really just a bunch of on-off switches arranged in a clever way to make adder circuits. Everything else a computer does is built out of these simple number operations. For example, text, images, and sound are all encoded with numbers that represent a certain character or a certain color. So at the simplest level <strong>a computer is not that different than a light switch</strong>—its just got trillions of these switches arranged in clever ways.</p>
<p><em>To learn more about how computers work, and the various levels of <strong>abstraction</strong> that make modern computing possible, I once again highly recommend <a href="%5Bhttps://www.youtube.com/playlist?list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo%5D(https://www.youtube.com/playlist?list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo)">Crash Course Computer Science</a>.</em></p>
<h3 id="the-takeaway">The Takeaway</h3>
<p>Aside from how awesome it is to understand how computers work, the main idea you need to take away from all of this is that computer systems are made of very simple basic elements. The complexity comes from combining many of those elements.</p>
<p>So too, as we learn to code, we will need to keep in mind that…</p>
<ul>
<li>Every bit of code is just a simple input, process,  and output.</li>
<li>Complex programs are just a lot of really simple code bundled together to make something amazing.</li>
</ul>
<p>Therefore, as long as you break things down and take code line by line, you will be able to see the simplicity in even the most complex code, and create great complexity of the simplest parts.</p>
</div>
</body>

</html>
