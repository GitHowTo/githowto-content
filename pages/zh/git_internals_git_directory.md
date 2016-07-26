---
view: page
title: "22. Inside Git: .Git directory"
---

<h3>Goals</h3>

<ul><li>To learn about Git directory structure<code>.git</code></li></ul>

<h2><em>01</em> The <code>.git</code> directory</h2>

<p>It is time to do some research. Starting from the project’s root directory...</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">ls -C .git</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ ls -C .git
COMMIT_EDITMSG	MERGE_RR	config		hooks		info		objects		rr-cache
HEAD		ORIG_HEAD	description	index		logs		refs</pre>

<p>This is a special folder where all the git stuff is. Let us explore the directory.</p>

<h2><em>02</em> Object Database</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">ls -C .git/objects</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ ls -C .git/objects
09	24	28	45	59	6a	77	80	8c	97	af	c4	e7	info
11	27	43	56	69	6b	78	84	91	9c	b5	e4	fa	pack</pre>

<p>You should see a lot of folders named with two characters. The first two letters sha1 hash of the object stored in git are the directory names.</p>

<h2><em>03</em> inquire the database objects</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">ls -C .git/objects/&lt;dir&gt;</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ ls -C .git/objects/09
6b74c56bfc6b40e754fc0725b8c70b2038b91e	9fb6f9d3a104feb32fcac22354c4d0e8a182c1</pre>

<p>Let us look at one of the folders named with two characters. There should be files with names of 38 characters. These files contain objects stored in git. They are compressed and encrypted, so it’s impossible to view their content directly. Let us have a better look at Git directory</p>

<h2><em>04</em> Config File</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cat .git/config</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ cat .git/config
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
	ignorecase = true
[user]
	name = Alexander Shvets
	email = alex@githowto.com</pre>

<p>This configuration file is created for each individual project. At least in this project, entries in this file will overwrite the entries in the <code>.gitconfig</code> file of your main directory.</p>

<h2><em>05</em> Branches and tags</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">ls .git/refs
ls .git/refs/heads
ls .git/refs/tags
cat .git/refs/tags/v1</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ ls .git/refs
heads
tags
$ ls .git/refs/heads
master
$ ls .git/refs/tags
v1
v1-beta
$ cat .git/refs/tags/v1
fa3c1411aa09441695a9e645d4371e8d749da1dc</pre>

<p>Files in tags subdirectory should be familiar to you. Each file corresponds to the tag previously created using the git tag command. Its content is nothing but a hash commit attached to the tag.</p>

<p>The <em>heads</em> folder is almost identical and is used not for tags, but branches. At the moment we have only one branch, and everything you see in this folder is a <em>master</em> branch.</p>

<h2><em>06</em> HEAD File</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">cat .git/HEAD</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ cat .git/HEAD
ref: refs/heads/master</pre>

<p>There is a reference to the current branch in the HEAD file. At the moment it must be the master branch.</p>