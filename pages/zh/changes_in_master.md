---
view: page
title: "26. Changes to master branch"
---

<h3>Goals</h3>

<ul><li>To learn how to work with several branches with different (sometimes conflicting) changes.</li></ul>

<p>At the time you are changing the style branch, someone decided to change the master branch. He added a README file.</p>

<h2><em>01</em> Update the README file with the changes.</h2>

<h4 class="h4-pre">File: <em>README</em></h4>

<pre class="file">This is the Hello World example from the git tutorial.</pre>

<h2><em>02</em> Commit changes of README file in the master branch.</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added README"</pre>