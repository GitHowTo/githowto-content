---
view: page
title: "39. What is origin?"
---

<h3>Goals</h3>

<ul><li>To learn about the naming of the remote repositories.</li></ul>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git remote</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git remote
origin</pre>

<p>We see that the cloned repository knows the default name of the remote repository.  To get more information about origin:</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git remote show origin</pre>

<h4 class="h4-pre">Result:</h4>

<pre class="sample">$ git remote show origin
* remote origin
  Fetch URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  Push  URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  HEAD branch (remote HEAD is ambiguous, may be one of the following):
    style
    master
  Remote branches:
    style  tracked
    master tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)</pre>

<p>We can see that the &#8220;origin&#8221; of the remote repository is the original <strong>hello</strong> repo.  Remote repos are typically stored on a separate machine or a centralized server.  However, as we see, they can also point to a repository on the same machine. There is nothing so special about the name &#8220;origin&#8221;, but there is a convention to use it for the primary centralized repository (if any).</p> 