---
view: page
title: "29. Creating a conflict"
---

<h3>Goals</h3>

<ul><li>Creating a conflicting of changes in the master branch.</li></ul>

<h2><em>01</em> Return to the master and create conflict</h2>

<p>Return to the master branch and make the following changes:</p>

<pre class="instructions">git checkout master</pre>

<h4 class="h4-pre">File: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- no style --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World! <strong>Life is great!</strong>&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m 'Life is great!'</pre>

(<b>Warning:</b> make sure you've used single-quotes to avoid problems with bash and <code>!</code> character)

<h2><em>02</em> View branches</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist --all
* 454ec68 2011-03-09 | Life is great! (HEAD, master) [Alexander Shvets]
| * 5813a3f 2011-03-09 | Merge branch 'master' into style (style) [Alexander Shvets]
| |\  
| |/  
|/| 
* | 6c0f848 2011-03-09 | Added README [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html [Alexander Shvets]
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

<p>After an Added README commit master branch has been merged with the style branch, but at there is an additional master commit, which was not merged back to the style.</p>

<h2><em>03</em> Next</h2>

<p>The last change in master conflicts with some changes in style. In the next step we will solve this conflict.</p>