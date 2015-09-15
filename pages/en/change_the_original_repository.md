---
view: page
title: "41. Changing the original repository"
---

<h3>Goals</h3>

<ul><li>To make changes to the original repository so we can try to pull the changes</li></ul>

<h2><em>01</em>Make a change in the original <strong>hello</strong> repository</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cd ../hello
# (You should be in the original hello repository now)</pre>

<p style="color:red;"><strong><span class="caps">NOTE</span>: We are now in the repository <em>hello</em></strong></p>

<p>Make the following changes to the <span class="caps">README</span> file:</p>

<h4 class="h4-pre">File: <em><span class="caps">README</span></em></h4>

<pre class="file">This is the Hello World example from the git tutorial.
(changed in original)</pre>

<p>Now add and commit this change</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add README
git commit -m "Changed README in original repo"</pre>

<h2><em>02</em> Next</h2>

<p>Now the original repo has more recent changes that are not included in the cloned version.  Next we will pull those changes across to the cloned repo.</p>
  </div>