---
view: page
title: "13. Tagging versions"
---

<h3>Goals</h3>

<ul><li>To learn how to tag commits for future references</li></ul>

<p>Let&#8217;s call the current version of the hello program version 1 (v1).</p>

<h2><em>01</em> Creating a tag of the first </h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git tag v1</pre>

<p>Now, the current version of the page is referred to as <em>v1</em>.</p>

<h2><em>02</em> Tags for previous versions </h2>

<p>Let&#8217;s tag the version prior to the current version with the name v1-beta.  First of all we will checkout the previous version.  Instead of looking up the hash, we are going to use the <code>^</code> notation indicating &#8220;the parent of v1&#8221;.</p>

<p class="note">If the <code>v1</code>^ notation causes troubles, try using <code>v1~1</code>, referencing the same version. This notation means &#8220;the first version prior to v1&#8221;.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout v1^
cat hello.html</pre>

<h4 class="h4-pre">Run:</h4>

<pre class="sample">$ git checkout v1^
Note: checking out 'v1^'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 8c32287... Added standard HTML page tags
$ cat hello.html
&lt;html&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>This is the version with <code>&lt;html&gt;</code> and <code>&lt;body&gt;</code> tags, but without <code>&lt;head&gt;</code>. Let&#8217;s make it’s the v1-beta version.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git tag v1-beta</pre>

<h2><em>03</em> Check out by the tag name </h2>

<p>Now try to checkout between the two tagged versions.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout v1
git checkout v1-beta</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout v1
Previous HEAD position was 8c32287... Added standard HTML page tags
HEAD is now at fa3c141... Added HTML header
$ git checkout v1-beta
Previous HEAD position was fa3c141... Added HTML header
HEAD is now at 8c32287... Added standard HTML page tags</pre>

<h2><em>04</em> Viewing tags with the <code>tag</code> command</h2>

<p>You can see the available tags using the <code>git tag</code> command.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git tag</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git tag
v1
v1-beta</pre>

<h2><em>05</em> Viewing tags in logs </h2>

<p>You can also check for tags in the log.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git hist master --all</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist master --all
* fa3c141 2011-03-09 | Added HTML header (v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (HEAD, v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>You can see tags (<code>v1</code> and <code>v1-beta</code>) listed in the log together with the name of the branch (<code>master</code>).  The <code>HEAD</code> shows the commit you checked out (currently <code>v1-beta</code>).</p>