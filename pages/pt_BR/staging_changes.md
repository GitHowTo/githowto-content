---
view: page
title: "6. Staging the changes"
---

<h3>Metas</h3>

<ul><li>To learn to stage changes for the upcoming commits</li></ul>

<h2><em>01</em> Adding changes</h2>

<p>Now command git to stage changes. Check the status</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html
git status</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git add hello.html
$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Changes to the hello.html have been staged. This means that git knows about the change, but it is not permanent in the repository. The next commit will include the changes staged.</p>

<p>Should you decide not to commit the change, the status command will remind you that you can use the <code>git reset</code> command to unstage these changes.</p>
