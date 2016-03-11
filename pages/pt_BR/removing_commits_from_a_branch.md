---
view: page
title: "17. Removing a commit from a branch"
---

<h3>Metas</h3>

<ul><li>To learn to delete the branch's latest commits</li></ul>

<p><code>Revert</code> is a powerful command of the previous section that allows you to cancel any commits to the repository. However, both original and cancelled commits are seen in the history of the branch (when using <code>git log</code> command).</p>

<p>Often after commit is already made, we realize that it was a mistake. It would be nice to have undo option command allowing deleting incorrect commit immediately. This command would prevent the appearance of unwanted commit in the <code>git log</code> history.</p>

<h2><em>01</em> The <code>reset</code> command</h2>

<p>We have already used reset command to match the buffer zone and the selected commit (HEAD commit was used in the previous lesson).</p>

<p>When a commit reference is given (ie, a branch, hash, or tag name), the <code>reset</code> command will...</p>

<ol>
<li>Overwrite the current branch so it will point to the correct commit</li>
<li>Optionally reset the buffer zone so it will comply with the specified commit</li>
<li>Optionally reset the working directory so it will match the specified commit</li>
</ol>

<h2><em>02</em> Check our history</h2>

<p>Let us do a quick scan of our commit history.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (HEAD, master) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>We see that the last two commits in this branch are "Oops" and "Revert Oops". Let us remove them with reset command.</p>

<h2><em>03</em> Mark this branch first</h2>

<p>Let us mark the last commit with tag, so you can find it after removing commits.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git tag oops</pre>

<h2><em>04</em> Reset commit to previous Oops</h2>

<p>At the history log (see above), the commit tagged «v1» is committing previous wrong commit. Let us reset the branch to that point. As the branch has a tag, we can use the tag name in the reset command (if it does not have a tag, we can use the hash value).</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git reset --hard v1
git hist</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git reset --hard v1
HEAD is now at fa3c141 Added HTML header
$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Our master branch is poiting at commit v1 and "Revert Oops" and "Oops" commits no longer exist in the branch. The  <code>--hard</code> parameter points out that the working directory must be updated to reflect the new branch head.</p>
<h2><em>05</em> Nothing is ever lost</h2>

<p>What happens to the wrong commits? They are still in the repository. Actually, we still can refer to them. At the beginning of the lesson, we created «oops» tag for the canceled commit. Let us take a look at <em>all</em> commits.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist --all
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (oops) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>We can see that the wrong commits haven’t gone. They are not listed in the master branch anymore but still remain in the repository. They would be still in the repository if we did not tag them, but then we could reference them only by their hash names. Unreferenced commits remain in the repository until the garbage collection software is run by system.</p>

<h2><em>06</em> Reset dangers</h2>

<p>Resets on local branches are usually harmless. The consequences of any "accident" can be reverted by using the proper commit.</p>

<p>Though, other users sharing the branch can be confused if the branch is shared on remote repositories.</p>
