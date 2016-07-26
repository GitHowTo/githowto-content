---
view: page
title: "25. Navigating Branches"
---

<h3>Goals</h3>

<ul><li>To learn how to navigate between the repository branches </li></ul>

<p>Now your project has two branches:</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist --all
* 07a2a46 2011-03-09 | Updated index.html (HEAD, style) [Alexander Shvets]
* 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. (master) [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<h2><em>01</em> Switching to the Master branch</h2>

<p>To switch between branches simply use the  <code>git checkout</code> command.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout master
cat lib/hello.html</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout master
Switched to branch 'master'
$ cat lib/hello.html
&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Now we are on the Master branch. It can be proven by the <code>hello.html</code> file that does not use styles from <code>style.css</code>.</p>

<h2><em>02</em> Let us return to the style branch.</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout style
cat lib/hello.html</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ cat lib/hello.html
&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>We are back to a <strong>style</strong> branch that can be proven by the contents of <code>lib/hello.html</code>.</p>