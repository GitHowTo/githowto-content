---
view: page
title: "30. Resolving Conflicts"
---

<h3>Goals</h3>

<ul><li>To learn to resolve merging conflicts </li></ul>

<h2><em>01</em> Merge the master branch with style</h2>

<p>Let us go back to the style branch and merge it with a new master branch.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout style
git merge master</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ git merge master
Auto-merging lib/hello.html
CONFLICT (content): Merge conflict in lib/hello.html
Automatic merge failed; fix conflicts and then commit the result.</pre>

<p>If you open the <code>lib/hello.html</code> you will see:</p>

<h4 class="h4-pre">File: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
&lt;&lt;&lt;&lt;&lt;&lt;&lt; HEAD
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
=======
    &lt;!-- no style --&gt;
&gt;&gt;&gt;&gt;&gt;&gt;&gt; master
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello,World! Life is great!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

<p>The first section is the version of the current branch (style) head. The second section is the version of master branch.</p>

<h2><em>02</em> Resolution of the conflict</h2>

<p>You need to resolve the conflict manually. Make changes to <code>lib/hello.html</code> to achieve the following result.</p>

<h4 class="h4-pre">File: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World! Life is great!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Make a commit of conflict resolution</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m "Merged master fixed conflict."</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git add lib/hello.html
$ git commit -m "Merged master fixed conflict."
Recorded resolution for 'lib/hello.html'.
[style 645c4e6] Merged master fixed conflict.</pre>

<h2><em>04</em> Advanced Merging</h2>

<p>Git has no graphical merging tools, but will accept any third-party merge tool (<a href="http://stackoverflow.com/questions/137102/whats-the-best-visual-merge-tool-for-git">read more about such tools on StackOverflow</a>.)</p>