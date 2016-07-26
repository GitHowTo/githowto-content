---
view: page
title: "42. Fetching changes"
---

<h3>Goals</h3>

<ul><li>To learn how to pull changes from a remote repository.</li></ul>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cd ../cloned_hello
git fetch
git hist --all</pre>

<p style="color:red;"><strong><span class="caps">NOTE</span>: We are now in the repository <em>cloned_hello</em></strong></p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git fetch
From /Users/alex/Documents/Presentations/githowto/auto/hello
   6e6c76a..2faa4ea  master     -&gt; origin/master
$ git hist --all
* 2faa4ea 2011-03-09 | Changed README in original repo (origin/master, origin/HEAD) [Alexander Shvets]
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, origin/style, master) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>At the moment the repository contains all the commits from the original repo, however they aren&#8217;t integrated into the local branches of the cloned repository.</p>

<p>You&#8217;ll find the commit named &#8220;Changed <span class="caps">README</span> in original repo&#8221; in the history.  Notice that the commit includes &#8220;origin/master&#8221; and &#8220;origin/<span class="caps">HEAD</span>&#8221;.</p>

<p>Now let&#8217;s take a look at the &#8220;Updated index.html&#8221; commit.  You&#8217;ll see that the local master branch points to this very commit, not the new commit we&#8217;ve just fetched.</p>

<p>This brings us to the conclusion that the &#8220;git fetch&#8221; command will fetch new commits from the remote repo, but won&#8217;t merge them into the local branches.</p>

<h2><em>01</em>Check the <span class="caps">README</span></h2>

<p>We can show that the cloned <span class="caps">README</span> file has not been changed.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cat README</pre>
<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.</pre>

<p>No changes, as you can see.</p>