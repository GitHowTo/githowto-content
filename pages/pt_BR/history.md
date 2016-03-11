---
view: page
title: "10. History"
---

<h3>Metas</h3>

<ul><li>To learn to view the project’s history.</li></ul>

<p>Getting a list of changes made is a function of the <code>git log</code> command.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git log</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git log
commit fa3c1411aa09441695a9e645d4371e8d749da1dc
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added HTML header

commit 8c3228730ed03116815a5cc682e8105e7d981928
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added standard HTML page tags

commit 43628f779cb333dd30d78186499f93638107f70b
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added h1 tag

commit 911e8c91caeab8d30ad16d56746cbd6eef72dc4c
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    First Commit</pre>

<p>Here is a list of all the four commits to the repository, which we were able to make so far.</p>

<h2><em>01</em> One line history</h2>

<p>You fully control over what the <code>log</code> shows. I like the single line format:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git log --pretty=oneline</pre>

<p>You will see &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git log --pretty=oneline
fa3c1411aa09441695a9e645d4371e8d749da1dc Added HTML header
8c3228730ed03116815a5cc682e8105e7d981928 Added standard HTML page tags
43628f779cb333dd30d78186499f93638107f70b Added h1 tag
911e8c91caeab8d30ad16d56746cbd6eef72dc4c First Commit</pre>

<h2><em>02</em> Controlling the display of entries</h2>

<p>There are many options to choose which entreis appear in the log. Play around with the following parameters:</p>

<pre class="instructions">git log --pretty=oneline --max-count=2
git log --pretty=oneline --since='5 minutes ago'
git log --pretty=oneline --until='5 minutes ago'
git log --pretty=oneline --author=&lt;your name&gt;
git log --pretty=oneline --all</pre>

<p>Details are provided in the <code>git-log</code> instruction.</p>

<h2><em>03</em> Getting fancy</h2>

<p>This is what I use to review the changes made within the last week. I will add <code>--author=alex</code> if I want to see only the changes made by me.</p>

<pre class="instructions">git log --all --pretty=format:"%h %cd %s (%an)" --since='7 days ago'</pre>

<h2><em>04</em> The ultimate format of the log</h2>

<p>Over time, I found the following log format to be the most suitable.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short</pre>

<p>It looks like this:</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Let&#8217;s look at it in detail:</p>

<ul><li><code>--pretty="..."</code> defines the output format.</li>
	<li><code>%h</code> is the abbreviated hash of the commit</li>
	<li><code>%d</code> commit decorations (e.g. branch heads or tags)</li>
	<li><code>%ad</code> is the commit date</li>
	<li><code>%s</code> is the comment</li>
	<li><code>%an</code> is the name of the author </li>
	<li><code>--graph</code> tells git to display the commit tree in the form of an <span class="caps">ASCII</span> graph layout</li>
	<li><code>--date=short</code> keeps the date format short and nice</li></ul>

<p>So, every time you want to see a log, you'll have to do a lot of typing. Fortunately, we will find out about the git aliases in the next lesson.</p>

<h2><em>05</em> Other tools</h2>

<p>Both <code>gitx</code> (for Mac) and <code>gitk</code> (for any platform) can help to explore log history.</p>
