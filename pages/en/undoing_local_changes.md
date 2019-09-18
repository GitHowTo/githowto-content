---
view: page
title: "14. Discarding local changes (before staging)"
---

<h3>Goals</h3>

<ul><li>To learn how to discard the working directory changes </li></ul>

<h2><em>01</em> Checking out the Master branch </h2>

<p>Make sure you are on the lastest commit in the master brach before you continue.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout master</pre>

<h2><em>02</em> Change hello.html </h2>

<p>It happens that you modify a file in your local working directory and sometimes wish just to discard the committed changes.  Here is when the checkout command will help you.</p>

<p>Make changes to the hello.html file in the form of an unwanted comment.</p>

<h4 class="h4-pre">File: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is a bad comment.  We want to revert it. --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Check the status </h2>

<p>First of all, check the working directory’s status.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git status</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>We see that the <code>hello.html</code> file has been modified, but not staged yet.</p>

<h2><em>04</em> Undoing the changes in the working directory</h2>

<p>Use the <code>checkout</code> command in order to checkout the repository&#8217;s version of the <code>hello.html</code> file.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git checkout hello.html
git status
cat hello.html</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git checkout hello.html
$ git status
# On branch master
nothing to commit (working directory clean)
$ cat hello.html
&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>The status command shows there were no unstaged changes in the working directory.  And the &#8220;bad comment&#8221; is no longer contained in the file.</p>