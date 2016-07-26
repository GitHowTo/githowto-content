---
view: page
title: "27. View the different branches"
---

<h3>Goals</h3>

<ul><li>To learn how to view the different branches in the repository.</li></ul>

<h2><em>01</em> View current branches</h2>

<p>Now we have a repository with two different branches. To view branches and their differences use log command as follows.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist --all
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

<p>We have opportunity to see <code>--graph</code> of <code>git hist</code> in action. Adding the <code>--graph</code> option to <code>git log</code> causes the construction of a commit tree with the help of simple ASCII characters. We see both branches (style and master) and that the current branch is master HEAD. The Added index.html branch goes prior to both branches.</p>

<p>The <code>--all</code> flag guarantees that we see all the branches. By default, only the current branch is displayed.</p>
