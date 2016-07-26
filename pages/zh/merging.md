---
view: page
title: "28. Merging"
---

<h3>Goals</h3>

<ul><li>To learn how to merge two distinct branches to restore changes to a single branch.</li></ul>

<h2><em>01</em> Merging to a single branch</h2>

<p>Merging brings changes from two branches into one. Let us go back to the style branch and merge it with master.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout style
git merge master
git hist --all</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ git merge master
Merge made by recursive.
 README |    1 +
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 README
$ git hist --all
*   5813a3f 2011-03-09 | Merge branch 'master' into style (HEAD, style) [Alexander Shvets]
|\  
| * 6c0f848 2011-03-09 | Added README (master) [Alexander Shvets]
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

<p>Through periodic master branch merging with the style branch you can pick up to the master any changes or modifications to maintain compatibility with the style changes in the mainline.</p>

<p>However, this makes the commit graphics look ugly. Later we will consider relocation as an alternative to fusion.</p>

<h2><em>02</em> Next</h2>

<p>But what if changes to the master branch conflict with changes in style?</p>