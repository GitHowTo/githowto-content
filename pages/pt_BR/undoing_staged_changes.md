---
view: page
title: "15. Cancel Staged changes (before committing)"
---

<h3>Metas</h3>

<ul><li>To learn how to undo changes that have been staged</li></ul>

<h2><em>01</em> Edit file and stage changes</h2>

<p>Make changes to the <code>hello.html</code> file in the form of an unwanted comment</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- This is an unwanted but staged comment --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Stage the modified file.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>02</em> Check the status </h2>

<p>Check the status of unwanted changes .</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Status shows that the change has been staged and is ready to commit.</p>

<h2><em>03</em> Reset the buffer zone</h2>

<p>Fortunately, the displayed status shows us exactly what we should do to cancel staged changes.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git reset HEAD hello.html</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git reset HEAD hello.html
Unstaged changes after reset:
M	hello.html</pre>

<p>The <code>reset</code> command resets the buffer zone to HEAD. This clears the buffer zone from the changes that we have just staged.</p>

<p>The <code>reset</code> command (default) does not change the working directory. Therefore, the working directory still contains unwanted comments. We can use the checkout command from the previous tutorial to remove unwanted changes from working directory.</p>

<h2><em>04</em> Switch to commit version</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout hello.html
git status</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>Our working directory is clean again.</p>
