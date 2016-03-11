---
view: page
title: "5. Making changes"
---

<h3>Metas</h3>

<ul><li>To learn to monitor the working directory’s state</li></ul>

<h2><em>01</em> Changing the “Hello, World” page</h2>

<p>Let&#8217;s add some HTML-tags to our greeting. Change the file contents to:</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;h1&gt;</strong>Hello, World!<strong>&lt;/h1&gt;</strong></pre>

<h2><em>02</em> Checking the status</h2>

<p>Check the working directory’s status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>The first important aspect here is that git knows <code>hello.html</code> file has been changed, but these changes are not yet committed to the repository.</p>

<p>Another aspect is that the status message hints about what to do next. If you want to add these changes to the repository, use <code>git add</code>. To undo the changes use <code>git checkout</code>.</p>

<h2><em>03</em> Next ...</h2>

<p>Staging the changes.</p>
