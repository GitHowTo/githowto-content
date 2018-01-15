---
view: page
title: "19. Changing commits"
---

<h3>Goals</h3>

<ul><li>To learn how to modify an already existing commit</li></ul>

<h2><em>01</em> Change the page and commit</h2>

<p>Post an author comment on the page.</p>

<h4 class="h4-pre">File: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add hello.html
git commit -m "Add an author comment"</pre>

<h2><em>02</em> Oops... email required</h2>

<p>After making the commit you understand that every good comment should include the author's email. Refresh the hello page, to provide an email.</p>

<h4 class="h4-pre">File: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Change the previous commit</h2>

<p>We do not want to create another commit for e-mail. Let us change the previous commit and add an e-mail address.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add hello.html
git commit --amend -m "Add an author/email comment"</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git add hello.html
$ git commit --amend -m "Add an author/email comment"
[master 6a78635] Add an author/email comment
 1 files changed, 2 insertions(+), 1 deletions(-)</pre>

<h2><em>04</em> View history</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist
* 6a78635 2011-03-09 | Add an author/email comment (HEAD, master) [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>The new "author/email" commit replaces the original "author" commit. The same effect can be achieved by resetting the last commit in the branch, and recommitting new changes.</p>
