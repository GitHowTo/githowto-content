---
view: page
title: "8. Commiting the changes"
---

<h3>Goals</h3>

<ul><li>To learn to commit to the repository</li></ul>

<h2><em>01</em> Committing changes </h2>

<p>Well, enough about staging.  Let&#8217;s commit the staged changes to the repository.</p>

<p>When you previously used <code>git commit</code> for committing the first <code>hello.html</code> version to the repository, you included the <code>-m</code> flag that gives a comment on the command line.  The commit command allows interactively editing comments for the commit.  And now, let&#8217;s see how it works.</p>

<p>If you omit the <code>-m</code> flag from the command line, git will pop you into the editor of your choice from the list (in order of priority):</p>

<ul>
<li>GIT_EDITOR environment variable</li>
<li>core.editor configuration setting</li>
<li><span class="caps">VISUAL</span> environment variable</li>
<li><span class="caps">EDITOR</span> environment variable</li>
</ul>

<p>I have the <span class="caps">EDITOR</span> variable set to <code>emacsclient</code> (available for Linux and Mac).</p>

<p>Let us commit now and check the status.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git commit</pre>

<p>You will see the following in your editor:</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">|
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>On the first line, enter the comment: &#8220;Added <span class="caps">hi tag</span>&#8221;.  Save the file and exit the editor (to do it in default editor, press ESC and then type <code>:wq</code> and hit Enter).  You should see &#8230</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">git commit
Waiting for Emacs...
[master 569aa96] Added h1 tag
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>"Waiting for Emacs&#8230;" is obtained from the <code>emacsclient</code> program sending the file to a running emacs program and waiting for it to be closed.  The rest of the data is the standard commit messages.</p>

<h2><em>02</em> Checking the status</h2>

<p>At the end let us check the status.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git status</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>The working directory is clean, you can continue working.</p>