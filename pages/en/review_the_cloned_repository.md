---
view: page
title: "38. Examine the cloned repository"
---

<h3>Goals</h3>

<ul><li>To find out about branches in the remote repositories.</li></ul>

<h2><em>01</em> Viewing the cloned repository</h2>

<p>Let&#8217;s have a look at our cloned repository.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cd cloned_hello
ls</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ cd cloned_hello
$ ls
README
index.html
lib</pre>

<p>You will see a list of all files in the top level of the original repository (<code>README</code>, <code>index.html</code> and <code>lib</code>).</p>

<h2><em>02</em> View the history of the repository</h2>

<h4 class="h4-pre">Run:</h4>
<pre class="instructions">git hist --all</pre>
<h4 class="h4-pre">Result:</h4>
<pre class="sample">$ git hist --all
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, origin/master, origin/style, origin/HEAD, master) [Alexander Shvets]
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

<p>You will see a list of all the commits in the new repository, and it should match the commit history of the original repository. The only difference should be in the names of the branches.</p>

<h2><em>03</em> Remote branches</h2>

<p>You will see a <strong>master</strong> branch (<strong><span class="caps">HEAD</span></strong>) in the history.  You will also find branches with strange names (<strong>origin/master</strong>, <strong>origin/style</strong> and <strong>origin/<span class="caps">HEAD</span></strong>).  We&#8217;ll discuss them a bit later.</p>