---
view: page
title: "40. Remote branches"
---

<h3>Goals</h3>

<ul><li>To learn about local and remote branches</li></ul>

<p>Let&#8217;s take a look at the branches in our cloned repository.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git branch</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git branch
* master</pre>

<p>As we can see only the master branch is listed in it. Where is the style branch? <code>git branch</code> only lists the local branches by default.</p>
<h2><em>01</em> 01 List of the remote branches</h2>

<p>To see all the branches, try the following command:</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git branch -a</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git branch -a
* master
  remotes/origin/HEAD -&gt; origin/master
  remotes/origin/style
  remotes/origin/master</pre>

<p>Git lists all the commits from the original repo, but the remote repository branches are not treated as local ones.  If we need our own <strong>style</strong> branch, we need to create on our own. In a minute you will see how it is done.</p>