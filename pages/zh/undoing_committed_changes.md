---
view: page
title: "十六、取消提交"
---

<h3>目标</h3>

<ul><li>学会如何撤销已提交至版本库中的对象。</li></ul>

<h2><em>01</em> 撤销提交</h2>

<p>有时你会发现新的提交出错了，并想撤销它们。有好几种方法都可以处理这种问题，而我们选择最安全的一种。</p>

<p>为了撤销提交对象，我们将先创建一个提交对象，然后再撤销这次意外的修改。</p>

<h2><em>02</em> 编辑文件，并进行提交</h2>

<p>使用以下内容替换<code>hello.html</code>文件。</p>

<h4 class="h4-pre">文件：<em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is an unwanted but committed change --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git add hello.html
git commit -m "Oops, we didn't want this commit"</pre>

<h2><em>03</em>用新的修改创建一个提交对象，并撤销之前的修改</h2>

<p>为了撤销提交，我们需要创建一个提交对象，以删除需要被撤销的提交中的修改。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git revert HEAD</pre>

<p>进入编辑器，编辑默认的提交注释或保持原样。保存并关闭文件。</p>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git revert HEAD --no-edit
[master 45fa96b] Revert "Oops, we didn't want this commit"
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>由于我们取消的是最新的一次提交，因此我们可以直接使用<code>HEAD</code>。我们也可以撤销历史中任意一次提交，只需要使用它的哈希值即可。</p>

<p class="note"><strong>注：</strong><code>--no-edit</code>命令参数可以省略。之前的操作不需要打开编辑器也可以产生我们预期的输出数据。</p>

<h2><em>04</em>查看历史记录</h2>

<p>查看历史记录以确认在版本库中需要被删除的提交对象已被撤销。</p>

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

<p>这个技巧可以被用于任何提交对象（虽然有可能会产生冲突）。它甚至可以在远程版本库中的公共分支上使用。</p>

<h2><em>05</em> 接下来</h2>

<p>接下来，让我们学习一个可以被用来删除版本库历史中上一次提交的技巧。</p>
