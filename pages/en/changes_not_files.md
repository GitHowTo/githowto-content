---
view: page
title: "9. Changes, not files"
---

<h3>Goals</h3>

<ul><li>Understanding that git works with the changes, not the files.</li></ul>

<p>Most version control systems work with files.  You add the file to source control and the system tracks changes from that moment on.</p>

<p>Git concentrates on the changes to a file, not the file itself. A <code>git add file</code> command does not tell git to add the file to the repository, but to note the current state of the file for it to be commited later.</p>

<p>We will try to investigate the difference in this lesson.</p>

<h2><em>01</em> First Change: Adding default page tags</h2>

<p>Change the &#8220;Hello, World&#8221; page so that it contained default tags <code>&lt;html&gt;</code> and <code>&lt;body&gt;</code>.</p>

<h4 class="h4-pre">File: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;html&gt;
  &lt;body&gt;</strong>
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  <strong>&lt;/body&gt;
&lt;/html&gt;</strong></pre>

<h2><em>02</em> Add this change</h2>

<p>Now add this change to the git staging.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>03</em> Second change: Add the HTML headers</h2>

<p>Now add the HTML headers (<code>&lt;head&gt;</code> section) to the &#8220;Hello, World&#8221; page.</p>

<h4 class="h4-pre">File: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>04</em> Check the current status</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git status</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#</pre>

<p>Please note that hello.html is listed in the status twice. The first change (the addition of default tags) is istaged and ready for a commit. The second change (adding HTML headers) is unstaged. If you were making a commit right now, headers would not have been saved to the repository.</p>

<p>Let&#8217;s check.</p>

<h2><em>05</em> Commit</h2>

<p>Commit the staged changes (default values), then check the status one more time.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git commit -m "Added standard HTML page tags"
git status</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git commit -m "Added standard HTML page tags"
[master 8c32287] Added standard HTML page tags
 1 files changed, 3 insertions(+), 1 deletions(-)
$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>The status command suggests that <code>hello.html</code> has unrecorded changes, but is no longer in the buffer zone.</p>

<h2><em>06</em> Adding the second change</h2>

<p>Add the second change to the staging area, after that run the <code>git status</code> command.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add .
git status</pre>

<p class="note"><strong>Note:</strong> The current directory (&#8216;.&#8217;) will be our file to add.  This is the most convenient way to add all the changes to the files of the current directory and its folders.  But since it adds everything, it is a good idea to check the status prior to doing an <tt>add .</tt>, to make sure you don&#8217;t add any file that should not be added.</p>

<p class="note">I wanted you to see the &#8220;add .&#8221; trick, and we will continue adding explicit files later on just in case.</p>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>The second change has been staged and is ready for a commit.</p>

<h2><em>07</em> Commit the second change</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git commit -m "Added HTML header"</pre>