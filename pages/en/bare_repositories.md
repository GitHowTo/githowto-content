---
view: page
title: "46. Bare repos"
---

<h3>Goals</h3>

<ul><li>To learn to create bare repos.</li></ul>

<p>Bare repos (without working directories) are typically needed for sharing.</p>

<h2><em>01</em>Creating a bare repository. </h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cd ..
git clone --bare hello hello.git
ls hello.git</pre>

<p style="color:red;"><strong><span class="caps">NOTE</span>: We are now in the working directory</strong></p>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git clone --bare hello hello.git
Cloning into bare repository hello.git...
done.
$ ls hello.git
HEAD
config
description
hooks
info
objects
packed-refs
refs</pre>

<p>Typically repositories ending in &#8216;.git&#8217; are bare.  As you can see there is no working directory in the hello.git repository.  Actually it is nothing but the .git directory of a non-bare repository.</p>
  </div>