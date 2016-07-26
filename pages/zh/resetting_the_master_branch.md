---
view: page
title: "33. Reset of the Master branch"
---

<h3>Goals</h3>

<ul><li>Reset the master branch to the point prior to the conflicting commit.</li></ul>

<h2><em>01</em> Resetting the master branch</h2>

<p> The interactive mode we added to the master branch has become a change conflicting with the changes in the style branch. Let&#8217;s revert the changes in the master branch up to the point before the conflict change was made.  This allows us to demonstrate the rebase command without having to worry about conflicts.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout master
git hist</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist
* 454ec68 2011-03-09 | Life is great! (HEAD, master) [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>The "Added <span class="caps">README</span>" commit goes directly before the conflicting interactive mode we added. Right now we need to reset the master branch to the "Added <span class="caps">README</span>" branch.</p>
<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git reset --hard &lt;hash&gt;
git hist --all</pre>

<p>Examine the log. It should look as if we rewound the repository to a point in time, prior to any mergers.</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git reset --hard 6c0f848
$ git hist --all
* 6c0f848 2011-03-09 | Added README (HEAD, master) [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html (style) [Alexander Shvets]
| * 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
| * 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>