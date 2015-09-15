---
view: page
title: "32. Resetting the style branch"
---

<h3>Goals</h3>

<ul><li>Resetting the branch style to the point prior to the first merge.</li></ul>

<h2><em>01</em> Resetting the style branch</h2>

<p>Let us go on style branch to the point <em>before</em> we merged it with master branch. We can <strong>reset</strong> branch to any commit. In fact, this changes branch pointer to point at any commit in the tree.</p>

<p>Here, we want to come back in style branch to a point before merging with the master. We have to find the last commit prior the merge.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout style
git hist</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout style
Already on 'style'
$ git hist
*   645c4e6 2011-03-09 | Merged master fixed conflict. (HEAD, style) [Alexander Shvets]
|\  
| * 454ec68 2011-03-09 | Life is great! (master) [Alexander Shvets]
* |   5813a3f 2011-03-09 | Merge branch 'master' into style [Alexander Shvets]
|\ \  
| |/  
| * 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* | 07a2a46 2011-03-09 | Updated index.html [Alexander Shvets]
* | 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
* | 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>It's a little hard to read, but we can see from the data that Updated index.html commit was the latest on the style branch prior merging. Let us reset the style branch to this commit.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git reset --hard &lt;hash&gt;</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git reset --hard 07a2a46
HEAD is now at 07a2a46 Updated index.html</pre>

<h2><em>02</em> Check the branch.</h2>

<p>Look for the style branch log. There are no merge commits In our history.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist --all
* 454ec68 2011-03-09 | Life is great! (master) [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html (HEAD, style) [Alexander Shvets]
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