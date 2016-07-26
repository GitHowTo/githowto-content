---
view: page
title: "20. Moving files"
---

<h3>Goals</h3>

<ul><li>To learn how to move a file within the repository.</li></ul>

<h2><em>01</em> Move the hello.html file to the <i>lib</i> directory</h2>
<p>Now we will create the structure of our repository. Let us move the page in the lib directory</p>
<h4 class="h4-pre">Run:</h4>
<pre class="instructions">mkdir lib
git mv hello.html lib
git status</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ mkdir lib
$ git mv hello.html lib
$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	renamed:    hello.html -&gt; lib/hello.html
#</pre>

<p>Moving files with git, we notify git about two things</p>

<ol><li>The <code>hello.html</code> file was deleted.</li>
<li>The <code>lib/hello.html</code> file was created.</li>
</ol><p>Both facts are staged immediately and ready for a commit. Git status command reports the file has been moved.</p>

<h2><em>02</em> One more way to move files</h2>

<p>A positive fact about git is that you don’t need to remember about version control to the moment when you need to commit code. What could happen if we were using the operating system command line instead of the git command to move files?</p>

<p>The following set of commands turned out to be identical to our last actions. It requires more work with same result.</p>

<p class="command"> We can do:</p>

<pre class="instructions">mkdir lib
mv hello.html lib
git add lib/hello.html
git rm hello.html</pre>

<h2><em>03</em> Commit new directory</h2>

<p>Let us commit this movement.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git commit -m "Moved hello.html to lib"</pre>