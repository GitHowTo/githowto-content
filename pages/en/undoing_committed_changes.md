---
view: page
title: "16. Cancelling commits"
---

<h3>Goals</h3>

<ul><li>To learn how to undo commits to the local repository.</li></ul>

<h2><em>01</em> Cancelling commits</h2>

<p>Sometimes you realize that the new commits are wrong, and you want to cancel them. There are several ways to handle the issue, and we use the safest here.</p>

<p>To cancel the commit we will create a new commit, cancelling the unwanted changes.</p>

<h2><em>02</em> Edit the file and make a commit</h2>

<p>Replace  <code>hello.html</code> with the following file.</p>

<h4 class="h4-pre">File: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is an unwanted but committed change --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add hello.html
git commit -m "Oops, we didn't want this commit"</pre>

<h2><em>03</em> Make a commit with new changes that discard previous changes </h2>

<p>To cancel the commit, we need to create a commit that deletes the changes saved by unwanted commit.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git revert HEAD</pre>

<p>Go to the editor, where you can edit the default commit message or leave it as is. Save and close the file.</p>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git revert HEAD --no-edit
[master 45fa96b] Revert "Oops, we didn't want this commit"
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>Since we have cancelled the last commit, we can use <code>HEAD</code> as the argument for cancelling. We may cancel any random commit in history, pointing out its hash value.</p>

<p class="note"><strong>Note:</strong> The <code>--no-edit</code> command can be ignored. It was necessary to generate the output data without opening the editor.</p>

<h2><em>04</em> Check the log</h2>

<p>Checking the log shows the unwanted cancellations and commits in our repository.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (HEAD, master) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>This technique can be applied to any commit (however there may be conflicts). It is safe to use even in public branches of remote repositories.</p>

<h2><em>05</em> Next</h2>

<p>Next let us look at the technique that can be used to remove the last commit from the history of the repository.</p>
