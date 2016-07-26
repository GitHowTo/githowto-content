---
view: page
title: "48. Submitting changes"
---

<h3>Goals</h3>

<ul><li>To learn how to submit changes to the remote repository.</li></ul>

<p>Since clean repository, usually shared on any network server, we need to send our changes to other repositories.
Start by creating a change to be sent. Edit the README file and do a commit</p>

<h4 class="h4-pre"> File: <em> README </em></h4>

<pre class="file">This is the Hello World example from the git tutorial.
(Changed in the original and pushed to shared)</pre>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added shared comment to readme"</pre>

<p>Now send changes to the shared repository.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git push shared master</pre>
<p><em>The common repository</em> is receiving sent us the changes. (Remember, we added it as a remote repository in the previous lesson).</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git push shared master
To ../hello.git
   2faa4ea..79f507c  master -&gt; master</pre>

<p class="note"><strong>Note:</strong>  We had to explicitly specify the master branch to submit changes. It can be configured automatically, but I always forget the command. For easy management of remote branches switch to «Git Remote Branch».</p>