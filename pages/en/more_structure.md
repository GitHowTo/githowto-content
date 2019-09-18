---
view: page
title: "21. More information about the structure"
---

<h3>Goals</h3>

<ul><li>Add one more file in our repository</li></ul>

<h2><em>01</em> Adding index.html</h2>

<p>Let us add an <code>index.html</code> file to the repository. The following file is perfect for this purpose.</p>

<h4 class="h4-pre">File: <em>index.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;body&gt;
    &lt;iframe src="lib/hello.html" width="200" height="200" /&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Add the file and make a commit.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git add index.html
git commit -m "Added index.html."</pre>

<p>Now when you open <code>index.html</code>, you should see a part of the hello page in a small window.</p>