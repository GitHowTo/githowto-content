---
view: page
title: "3. Creating a Project"
---

<h3>Goals</h3>

<ul><li>To learn how to create a git repository from scratch.</li></ul>

<h2><em>01</em> Create a “Hello, World” page</h2>

<p>Get started in an empty working directory (for example, Work, if you downloaded the file from the previous step) and create an empty directory named “hello”, then create a <code>hello.html</code> file in it with the following contents.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">mkdir hello
cd hello
touch hello.html</pre>

<h4 class="h4-pre">File: <em>hello.html</em></h4>

<pre class="file">Hello, World</pre>

<h2><em>02</em> Create a repository</h2>

<p>So you have a directory that contains one file. Run the git init in order to create a git repo from that directory.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git init</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git init
Initialized empty Git repository in /Users/alex/Documents/Presentations/githowto/auto/hello/.git/
</pre>

<h2><em>03</em> Add the page to the repository</h2>

<p>Now let&#8217;s add the “Hello, World” page to the repository.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add hello.html
git commit -m "First Commit"</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git add hello.html
$ git commit -m "First Commit"
[master (root-commit) 911e8c9] First Commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 hello.html</pre>