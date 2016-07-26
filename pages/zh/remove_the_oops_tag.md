---
view: page
title: "18. Removing the oops tag"
---

<h3>Goals</h3>

<ul><li>Removing the oops tag (cleaning up)</li></ul>

<h2><em>01</em> Removal of the oops tag</h2>

<p>Oops tag has performed it’s function. Let us remove that tag and permit the garbage collector to delete referenced commit.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git tag -d oops
git hist --all</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git tag -d oops
Deleted tag 'oops' (was 45fa96b)
$ git hist --all
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Oops tag will no longer appear in the repository.</p>