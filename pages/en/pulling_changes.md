---
view: page
title: "44. Pulling and merging changes"
---

<h3>Goals</h3>

<ul><li>To learn that <code>git pull</code> command is identical to <code>git fetch</code> plus <code>git merge</code>.</li></ul>

<h3>Discussion</h3>

<p>We are not going to run through the entire process of making and pulling a new change, but we want you to know that: </p>

<pre class="instructions">git pull</pre>

<p>is actually equivalent to the following two steps:</p>

<pre class="instructions">git fetch
git merge origin/master</pre>