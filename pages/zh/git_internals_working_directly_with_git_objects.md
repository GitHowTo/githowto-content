---
view: page
title: "23. Git inside: Direct work with git objects"
---

<h3>Goals</h3>

<ul>
<li>Explore the structure of the database objects</li>
<li>Using SHA1 hashes for searching the content in repository</li>
</ul>

<p>Let us examine git objects with some tools.</p>

<h2><em>01</em> Searching for the last commit</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git hist --max-count=1</pre>

<p>This command should find the last commit in the repository. SHA1 hash is probably different on our systems; however you should see something like this.</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git hist --max-count=1
* 8029c07 2011-03-09 | Added index.html. (HEAD, master) [Alexander Shvets]</pre>

<h2><em>02</em> Display of the last commit</h2>

<p>With SHA1 hash of a commit, as above...</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git cat-file -t &lt;hash&gt;
git cat-file -p &lt;hash&gt;</pre>

<p>I see this ...</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git cat-file -t 8029c07
commit
$ git cat-file -p 8029c07
tree 096b74c56bfc6b40e754fc0725b8c70b2038b91e
parent 567948ac55daa723807c0c16e34c76797efbcbed
author Alexander Shvets &lt;alex@githowto.com&gt; 1299684476 -0500
committer Alexander Shvets &lt;alex@githowto.com&gt; 1299684476 -0500

Added index.html.</pre>

<p class="note"><strong>Note:</strong> If you specify the alias as «type» and «dump», as described in the corresponding lesson, you can enter commands <code>git type</code> and  <code>git dump</code> instead of a long command (which I never memorize).</p>

<p>This displays the commit object, which is in the head of master branch.</p>

<h2><em>03</em> Tree search</h2>

<p>We can display the tree referenced in the commit. This should be a file description (top level) in our project (for a specific commit). Use the SHA1 hash of the tree string from the list above.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git cat-file -p &lt;treehash&gt;</pre>

<p>Here is my tree ...</p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git cat-file -p 096b74c
100644 blob 28e0e9d6ea7e25f35ec64a43f569b550e8386f90	index.html
040000 tree e46f374f5b36c6f02fb3e9e922b79044f754d795	lib</pre>

<p>I can see the <code>index.html</code> file and lib folder.</p>

<h2><em>04</em> Display lib directory</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git cat-file -p &lt;libhash&gt;</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git cat-file -p e46f374
100644 blob c45f26b6fdc7db6ba779fc4c385d9d24fc12cf72	hello.html</pre>

<p>There is a <code>hello.html</code> file.</p>

<h2><em>05</em> Display <code>hello.html</code> file</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git cat-file -p &lt;hellohash&gt;</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git cat-file -p c45f26b
&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>And there it is. Tree objects, commit objects and blob objects are displayed directly from the git repository. That's all there is - trees, blobs and commits.</p>

<h2><em>06</em> Explore  by yourself</h2>

<p>The git repository can be explored manually. Try to manually find the original <code>hello.html</code> file from the first commit with help of SHA1 hash references in the last commit.</p>