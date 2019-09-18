---
view: page
title: "1. Preparation"
---

<h3>Goals</h3>

<ul><li>To be fully prepared to work with Git.</li></ul>

<h2><em>01</em> Setting up name and e-mail address</h2>

<p>If you've never used git before, first you need to set up your name and e-mail. Run the following commands to let git know your name and e-mail address. If git is already installed, skip down to the end of the line.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git config --global user.name "Your Name"
git config --global user.email "your_email@whatever.com"</pre>

<h2><em>02</em> Installation Options line endings</h2>

<p>Also, for users of Unix/Mac:</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git config --global core.autocrlf input
git config --global core.safecrlf true</pre>

<p>For Windows users:</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git config --global core.autocrlf true
git config --global core.safecrlf true</pre>