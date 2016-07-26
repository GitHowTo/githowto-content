---
view: page
title: "37. Cloning repositories"
---

<h3>Goals</h3>

<ul><li>To learn to make copies of the repositories.</li></ul>

<p>If you are working in a team, the following 12 chapters are quite important to understand because you almost always have to work with cloned repositories.</p>

<h2><em>01</em> Go to your working directory </h2>

<p>Go to the working directory and clone your hello repository.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cd ..
pwd
ls</pre>

<p style="color:red;"><strong><span class="caps">NOTE</span>: Now we are in the work directory.</strong></p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ cd ..
$ pwd
/Users/alex/Documents/Presentations/githowto/auto
$ ls
hello</pre>

<p>At this point you should be in your &#8220;working&#8221; directory.  It should contain a single repository named &#8220;hello&#8221;.</p>
<h2><em>02</em> Create a clone of the hello repository </h2>

<p>Let&#8217;s create a clone of the repository.</p>

<h4 class="h4-pre">Run:</h4>
<pre class="instructions">git clone hello cloned_hello
ls</pre>
<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git clone hello cloned_hello
Cloning into cloned_hello...
done.
$ ls
cloned_hello
hello</pre>

<p>Right now there should now be two repos in your working directory: the original &#8220;hello&#8221; repo and the cloned repository named &#8220;cloned_hello&#8221;.</p>