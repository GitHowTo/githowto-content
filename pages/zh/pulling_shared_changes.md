---
view: page
title: "49. Removing common changes"
---

<h3>Goals</h3>

<ul><li>To learn how to extract changes from the common repository.</li></ul>

<p>Quickly switch to the cloned repository and extract the changes, just sent in a common repository.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cd ../cloned_hello</pre>

<p style="color:red;"><strong>Note: We are now in the <em>cloned_hello</em> repository.</strong></p>

<p>Continue with …</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git remote add shared ../hello.git
git branch --track shared master
git pull
cat README</pre>