---
view: page
title: "7. Staging and committing"
---

<p>A staging step in git allows you to continue making changes to the working directory, and when you decide you wanna interact with version control, it allows you to record changes in small commits.</p>

<p>Suppose you have edited three files (<code>a.html</code>, <code>b.html</code>, and <code>c.html</code>).  After that you need to commit all the changes so that the changes to <code>a.html</code> and <code>b.html</code> were a single commit, while the changes to <code>c.html</code> were not logically associated with the first two files and were done in a separate commit.</p>

<p>In theory you can do the following:</p>

<pre class="instructions">git add a.html
git add b.html
git commit -m "Changes for a and b"</pre>

<pre class="instructions">git add c.html
git commit -m "Unrelated change to c"</pre>

<p>Separating staging and committing, you get the chance to easily customize what goes into a commit.</p>
