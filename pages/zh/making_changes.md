---
view: page
title: "五、做出修改"
---

<h3>目标</h3>

<ul><li>学会监控工作目录的状态</li></ul>

<h2><em>01</em> 修改『Hello, World』页面</h2>

<p>让我们在之前的问候语上添加一些HTML标签（HTML-tags）。将文件修改成如下内容：</p>

<h4 class="h4-pre">文件：<em>hello.html</em></h4>

<pre class="file"><strong>&lt;h1&gt;</strong>Hello, World!<strong>&lt;/h1&gt;</strong></pre>

<h2><em>02</em> 检查状态</h2>

<p>检查工作目录的状态。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git status</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>其中第一个重要的方面是git知道<code>hello.html</code>文件发生了修改，但这些修改还没有提交到版本库中。</p>

<p>另一方面是该状态消息提示了接下来需要做什么。如果你想将这些修改添加到版本库中，使用<code>git add</code>命令。如果想撤销这些修改，则使用<code>git checkout</code>命令。</p>

<h2><em>03</em> 接下来……</h2>

<p>暂存修改</p>
