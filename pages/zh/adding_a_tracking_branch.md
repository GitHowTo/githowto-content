---
view: page
title: "45. Adding a tracking branch"
---

<h3>Goals</h3>

<ul><li>To learn how to add a local branch that tracks a remote branch.</li></ul>

<p>Branches that start with remotes/origin belong to the the original repository.  Note that you don&#8217;t have a style branch anymore, but it knows that it was in the original repository.</p>

<h2><em>01</em> Add a local branch tracking the remote branch.</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git branch --track style origin/style
git branch -a
git hist --max-count=2</pre>

<h4 class="h4-pre">Result:</h4>
<pre class="sample">$ git branch --track style origin/style
Branch style set up to track remote branch style from origin.
$ git branch -a
  style
* master
  remotes/origin/HEAD -&gt; origin/master
  remotes/origin/style
  remotes/origin/master
$ git hist --max-count=2
* 2faa4ea 2011-03-09 | Changed README in original repo (HEAD, origin/master, origin/HEAD, master) [Alexander Shvets]
* 6e6c76a 2011-03-09 | Updated index.html (origin/style, style) [Alexander Shvets]</pre>

<p>Now we can see the style branch in the branch list and log.</p> 