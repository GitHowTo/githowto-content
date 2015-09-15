---
view: page
title: "35. Merging to the Master branch"
---

<h3>Goals</h3>

<ul><li>We have kept our style greet branch up to date with the master branch (using rebase), but now let&#8217;s merge the style branch changes back into the master.</li></ul>

<h2><em>01</em> Merging style into master</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout master
git merge style</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout master
Switched to branch 'master'
$
$ git merge style
Updating 6c0f848..6e6c76a
Fast-forward
 index.html       |    2 +-
 lib/style.css |    8 ++++++++
 lib/hello.html   |    6 ++++--
 3 files changed, 13 insertions(+), 3 deletions(-)
 create mode 100644 lib/style.css</pre>

<p> Since the last master commit directly precedes the last commit of the style branch, git can merge fast-forward by simply moving the branch pointer forward, pointing to the same commit as the style branch.</p>

<p>Conflicts do not arise in the fast-forward merge.</p>

<h2><em>02</em> Check the logs </h2>

<h4 class="h4-pre">Run:</h4>
<pre class="instructions">git hist</pre>
<h4 class="h4-pre">Result:</h4>
<pre class="sample">$ git hist
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, master, style) [Alexander Shvets]
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

<p>Now style and master are identical.</p>