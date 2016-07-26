---
view: page
title: "24. Creating a Branch"
---

<h3>Goals</h3>

<ul><li>To learn how to create a local branch in the repository</li></ul>

<p>It is time to make our hello world more expressive. Since it may take some time, it is best to move these changes into a new branch to isolate them from master branch changes.</p>

<h2><em>01</em> Create a branch</h2>

<p>Let us name our new branch «style».</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout -b style
git status</pre>

<p class="note"><strong>Note: </strong><code>git checkout -b &lt;branch name&gt;</code> is the shortcuts for <code>git branch &lt;branch name&gt;</code> followed by a <code>git checkout &lt;branch name&gt;</code>.</p>

<p>Note that the <code>git status</code> command reports that you are in the style branch.</p>

<h2><em>02</em>Add style.css file</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">touch lib/style.css</pre>

<h4 class="h4-pre">File: <em>lib/style.css</em></h4>

<pre class="file">h1 {
  color: red;
}</pre>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add lib/style.css
git commit -m "Added css stylesheet"</pre>

<h2><em>03</em>Change the main page</h2>

<p>Update the <code>hello.html</code> file, to use style.css.</p>

<h4 class="h4-pre">File: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
<strong>    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m "Hello uses style.css"</pre>

<h2><em>04</em>Change index.html</h2>

<p>Update the <code>index.html</code> file,so it could use <code>style.css</code></p>

<h4 class="h4-pre">File: <em>index.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="lib/style.css" /&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;iframe src="lib/hello.html" width="200" height="200" /&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add index.html
git commit -m "Updated index.html"</pre>

<h2><em>05</em> Next</h2>

<p>We now have a new branch named style with three new commits. Next lesson will show how to navigate and switch between branches.</p>