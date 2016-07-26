---
view: page
title: "四、查看版本库的状态"
---

<h3>目标</h3>

<ul><li>学习如何查看版本库的状态</li></ul>

<h2><em>01</em> 查看版本库的状态</h2>

<p>使用<code>git status</code>命令，查看版本库的当前状态。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git status</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>该命令检查了当前的状态并报告没有任何可以提交的修改，这表明版本库中保存的就是工作目录的当前状态，没有任何修改记录。</p>

<p>我们会使用 git status 命令频繁地检查工作目录与版本库的状态。</p>
