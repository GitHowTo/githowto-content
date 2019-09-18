---
view: page
title: "43. Merging pulled changes"
---

<h3>Goals</h3>

<ul><li>To learn to get the fetched changes into the current branch and working directory.</li></ul>

<h2><em>01</em>Merge the pulled changes into the local master branch</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git merge origin/master</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git merge origin/master
Updating 6e6c76a..2faa4ea
Fast-forward
 README |    1 +
 1 files changed, 1 insertions(+), 0 deletions(-)</pre>

<h2><em>02</em>Check the <span class="caps">README</span> again</h2>

<p>Now we should see the changes.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cat README</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.
(changed in original)</pre>

<p>These are the changes.  Although &#8220;git fetch&#8221; does not merge the changes, we can manually merge them from the remote repo.</p>

<h2><em>03</em>Next</h2>
<p>Now let&#8217;s have a look at combining fetch &amp; merge into a single command.</p>