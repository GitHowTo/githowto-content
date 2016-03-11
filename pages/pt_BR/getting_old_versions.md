---
view: page
title: "12. Getting older versions"
---

<h3>Metas</h3>

<ul><li>To learn how to checkout any previous snapshot into the working directory.</li></ul>

<p>Going back in history is very simple.  The checkout command can copy any snapshot from the repo to the working directory.</p>

<h2><em>01</em> Getting hashes for the previous versions</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist</pre>

<p class="note"><strong>Note:</strong> Do not forget to define <code>hist</code> in your <code>.gitconfig</code> file?  If you do not remember how, review the lesson on aliases.</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Check the log data and find the hash for the first commit.  You will find it in the last line of the <code>git hist</code> data.  Use the code (its first 7 chars are enough) in the command below.  After that check the contents of the hello.html file.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout &lt;hash&gt;
cat hello.html</pre>

<p class="note"><strong>Note:</strong> Many commands depend on the hash values in the repository. Since my hash values will be different from yours, substitute in the appropriate hash value for your repository everytime you see <code>&lt;hash&gt;</code> or <code>&lt;treehash&gt;</code> in the command.</p>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout 911e8c9
Note: checking out '911e8c9'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 911e8c9... First Commit
$ cat hello.html
Hello, World</pre>

<p>The <code>checkout</code> command output totally clarifies the situation.  Older git versions will complain about not being on a local branch.  But you don&#8217;t need to worry about that right now.</p>

<p>Note that the content of the hello.html file is the default content.</p>

<h2><em>02</em> Returning to the latest version in the master branch </h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
cat hello.html</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout master
Previous HEAD position was 911e8c9... First Commit
Switched to branch 'master'
$ cat hello.html
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

<p>&#8216;master&#8217; is the name of the default branch.  By checking out a branch by name, you go to its lastest version.</p>
