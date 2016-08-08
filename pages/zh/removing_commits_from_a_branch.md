---
view: page
title: "十七、从分支中删除一个提交对象"
---

<h3>目标</h3>

<ul><li>学会删除分支中的最近一次提交对象</li></ul>

<p>上一课中介绍的强大的<code>Revert</code>命令允许我们撤销版本库中的任何提交。但使用该命令会使得原提交对象与撤销操作提交对象两者均存在于分支的历史记录中（当使用<code>git log</code>命令查看时）。</p>

<p>通常情况下，当我们发现刚被提交的修改出了错时，最好有个回撤的选项能够将错误的提交立刻删除。而该命令也应该使出错的提交对象不再出现在<code>git log</code>历史记录中。</p>

<h2><em>01</em><code>reset</code>命令</h2>

<p>我们已经使用重置命令（reset）使被选择的提交对象置换缓冲区的内容（在前面的课程中，使用了HEAD提交对象）。</p>

<p>When a commit reference is given (ie, a branch, hash, or tag name), the <code>reset</code> command will...</p>
<p>当给定一个提交对象的引用符（例如，一个分支名、哈希值或者标签名），<code>reset</code>命令将会：</p>

<ol>
<li>覆盖当前的分支，使其指向给定的提交对象</li>
<li>可选择地重置缓冲区，以使其与指定的提交对象相吻合</li>
<li>可选择地重置工作目录，以使其与指定的提交对象相吻合</li>
</ol>

<h2><em>02</em> 查看历史记录</h2>

<p>让我们快速浏览一下提交的历史记录。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git hist
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (HEAD, master) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>我们可以看到该分支中最新的两次提交分别是『Oops』和『Revert Oops』。接下来让我们用reset命令删除它们。</p>

<h2><em>03</em> 首先对该分支进行标记</h2>

<p>让我们给最后一次提交对象打上标签，以便我们在删除操作后对其进行查找。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git tag oops</pre>

<h2><em>04</em> 将提交对象重置为之前一次错误修改（Oops）</h2>

<p>在上面显示的历史记录中，被标为«v1»的提交对象处于错误提交的前一个位置。让我们将该分支重置到那一点。由于该分支上有一个标签，我们可以在重置命令中使用标签名（在没有标签的情况下，我们可以使用哈希值）。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git reset --hard v1
git hist</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git reset --hard v1
HEAD is now at fa3c141 Added HTML header
$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>我们的主分支已经指向了v1提交对象，而『Revert Oops』和『Oops』提交对象已经不见了。<code>--hard</code>参数表明当前工作目录也必须同时被更新，以反映新的分支头指针。</p>

<h2><em>05</em>（实际上）没有任何东西被永远删除</h2>

<p>那么之前那些错误的提交去哪儿了？它们其实依然在版本库中。事实上，我们仍旧可以引用它们。在本课开始的时候，我们为被删除的提交对象创建了一个名为«oops»的标签。让我们来查看一下<em>所有的</em>（<em>all</em>）提交对象。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git hist --all
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (oops) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>我们可以看到之前错误的提交对象依旧存在。他们已经不再出现在主分支的提交列表里，但仍然存在于版本库中。如果我们不给它们打上标签它们也会存在，只是那样一来我们只能通过哈希值对它们进行引用。未被引用的提交对象会一直存在于版本库中，直到系统中运行垃圾回收软件。</p>

<h2><em>06</em> 重置操作的危险性</h2>

<p>在本地分支中进行重置操作一般是无害的。任何『意外修改』的后果都可以通过恰当的提交操作进行撤销。</p>

<p>但是，如果该分支在远程版本库中进行了共享，那么共享该分支的其他用户就会被这种操作弄混乱。</p>
