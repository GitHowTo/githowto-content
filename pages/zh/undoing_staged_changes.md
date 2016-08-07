---
view: page
title: "十五、（在提交之前）取消暂存的修改"
---

<h3>目标</h3>

<ul><li>学会如何撤销已被暂存的修改</li></ul>

<h2><em>01</em> 编辑文件，并暂存修改</h2>

<p>在<code>hello.html</code>文件中添加一句无用的注释。</p>

<h4 class="h4-pre">文件：<em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- This is an unwanted but staged comment --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>暂存被修改的文件。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>02</em> 查看状态 </h2>

<p>查看需撤销的修改的状态</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git status</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>状态结果表明本次修改已被暂存并准备好可以提交。</p>

<h2><em>03</em> 重置缓冲区</h2>

<p>幸运的是，状态信息准确无误地告诉了我们应该如何撤销已暂存的修改。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git reset HEAD hello.html</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git reset HEAD hello.html
Unstaged changes after reset:
M	hello.html</pre>

<p><code>reset</code>命令将缓冲区重置至HEAD。它清空了我们刚刚暂存至缓冲区的修改。</p>

<p><code>reset</code>命令（在默认的情况下）并不修改工作目录。因此，工作目录任然保存着之前的修改。我们可以使用上一课程中学习过的切换命令（checkout）撤销工作目录中的修改。</p>

<h2><em>04</em> 切换至提交版本</h2>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git checkout hello.html
git status</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>我们的工作目录又一次成为了干净的状态。</p>
