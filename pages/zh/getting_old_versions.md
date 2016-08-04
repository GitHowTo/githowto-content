---
view: page
title: "十二、获取旧的版本"
---

<h3>目标</h3>

<ul><li>学会如何切换至工作目录中之前的快照。</li></ul>

<p>回到历史其实非常简单。切换命令（checkout）可以将版本库中的任何快照复制到工作目录中。</p>

<h2><em>01</em> 获取之前版本的哈希值</h2>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git hist</pre>

<p class="note"><strong>注：</strong>别忘了在你的<code>.gitconfig</code>配置文件中定义<code>hist</code>别名。如果你不记得如何设置，请复习讲解别名的课程。</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>查看记录数据并找出第一次提交对象的哈希值。你将会在<code>git hist</code>命令结果中的最后一行找到该数据。在接下来的命令中使用该值（使用哈希值的前7位字符即可）。随后检查hello.html文件中的内容。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git checkout &lt;hash&gt;
cat hello.html</pre>

<p class="note"><strong>注：</strong> 许多命令都会依赖版本库中的哈希值。由于我的哈希值与你的并不一样，所以每当你在命令中看到<code>&lt;hash&gt;</code>或<code>&lt;treehash&gt;</code>时，都需要将其替换成为你自己版本库中相应的哈希值。</p>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

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

<p><code>checkout</code>命令的输出已经很清楚的说明了情况。更旧的git版本会提示在本地分支的警告。但是目前你还不必为此担心。</p>

<p>可以注意到hello.html文件的内容已经变回了其最初默认的样子。</p>

<h2><em>02</em> 回到主分支（master）中最新的版本</h2>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git checkout master
cat hello.html</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

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

<p>「master」是默认分支的名字。通过名字进行分支切换，你将会得到该分支的最新版本。</p>
