---
view: page
title: "十、历史"
---

<h3>目标</h3>

<ul><li>学会如何查看项目的历史。</li></ul>

<p><code>git log</code>命令的功能是获取所有已经提交的修改的列表。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git log</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

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

<p>结果展示了到目前为止我们提交到版本库中的所有四次修改。</p>

<h2><em>01</em> 单行历史</h2>

<p>你可以完全控制<code>log</code>展示的结果。我自己喜欢单行结果的格式：</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git log --pretty=oneline</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git log --pretty=oneline
fa3c1411aa09441695a9e645d4371e8d749da1dc Added HTML header
8c3228730ed03116815a5cc682e8105e7d981928 Added standard HTML page tags
43628f779cb333dd30d78186499f93638107f70b Added h1 tag
911e8c91caeab8d30ad16d56746cbd6eef72dc4c First Commit</pre>

<h2><em>02</em> 控制展示条目</h2>

<p>git提供了许多选项用于控制在历史记录（log）中展示的字段。可以试试以下这些参数：</p>

<pre class="instructions">git log --pretty=oneline --max-count=2
git log --pretty=oneline --since='5 minutes ago'
git log --pretty=oneline --until='5 minutes ago'
git log --pretty=oneline --author=&lt;your name&gt;
git log --pretty=oneline --all</pre>

<p><code>git-log</code>的文档中提供了详细的说明。</p>

<h2><em>03</em> 更强大的功能</h2>

<p>以下是我用于回顾在过去一周内发生的修改。如果我只想查看由我做出的修改，我还会使用<code>--author=alex</code>参数。</p>

<pre class="instructions">git log --all --pretty=format:"%h %cd %s (%an)" --since='7 days ago'</pre>

<h2><em>04</em> 历史记录（log）的终极格式</h2>

<p>久而久之，我发现以下的log格式设置最为合适。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short</pre>

<p>它的结果看起来像以下这样：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>让我们更仔细地对其进行说明：</p>

<ul><li><code>--pretty="..."</code>其中的内容定义了输出格式</li>
	<li><code>%h</code>是提交对象的简短的哈希值</li>
	<li><code>%d</code>是提交对象的修饰信息（例如分支的头指针或标签）</li>
	<li><code>%ad</code>是提交日期</li>
	<li><code>%s</code>是提交的注释</li>
	<li><code>%an</code>是作者的姓名</li>
	<li><code>--graph</code>该参数使git以ASCII图形显示提交操作的树状图</li>
	<li><code>--date=short</code>显示简短好看的日期格式</li></ul>

<p>看起来每当你想查看历史记录时都得要输入这么一长串命令。但幸运的是，git拥有别名（aliases）功能，我们将会在下一课教程中进行学习。</p>

<h2><em>05</em> 其它的工具</h2>

<p><code>gitx</code>（适用于Mac）和<code>gitk</code>（适用于任何平台）两个命令同样也可以帮助查看历史记录。</p>
