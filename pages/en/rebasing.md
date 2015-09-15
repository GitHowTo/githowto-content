---
view: page
title: "34. Rebase"
---

<h3>Goals</h3>

<ul><li>To use rebase instead of the merge command.</li></ul>

<p>So we went back in history before the first merge and wanna relocate the changes in master to our style branch.</p>

<p>This time we are going to use the rebase command rather than merge.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout style
git rebase master
git hist</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$
$ git rebase master
First, rewinding head to replay your work on top of it...
Applying: Added css stylesheet
Applying: Hello uses style.css
Applying: Updated index.html
$
$ git hist
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, style) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README (master) [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<h2><em>01</em> Merging VS rebasing</h2>

<p>Result of the rebase command looks much like that of the merge.  The style branch currently contains all its changes, plus all the changes of the master branch.  The commit tree, however, is a bit different.  The style branch commit tree has been rewritten to make the master branch a part of the commit history.  This makes the chain of commits linear and more readable.</p>

<h2><em>02</em> When to use the rebase, when the merge?</h2>

<p>Don&#8217;t use the rebase command &#8230;</p>

<ol>
	<li>If the branch is public and shared.  Rewriting such branches will hinder the work of other team members.</li>
	<li>When the <em>exact</em> commit branch history is important (because the rebase command rewrites the history of commits).</li>
</ol>
<p>Given the above recommendations, I prefer to use rebase for short-term, local branches and the merge command for branches in the public repository.</p>
  </div>