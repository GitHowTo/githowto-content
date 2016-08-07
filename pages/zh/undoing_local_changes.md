---
view: page
title: "十四、（在暂存之前）撤销本地修改"
---

<h3>目标</h3>

<ul><li>学会如何撤销在工作目录中的修改</li></ul>

<h2><em>01</em> 切换至主分支（Master）</h2>

<p>再继续学习之前先确保你处于主分支的最新一次提交对象上。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git checkout master</pre>

<h2><em>02</em> 修改hello.html文件 </h2>

<p>有时候你在工作目录中修改完一个文件，但随即又想撤销这些刚作出的修改。这时便可以使用切换命令（checkout）来达成目标。</p>

<p>在hello.html文件中添加一句无用的注释。</p>

<h4 class="h4-pre">File: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is a bad comment.  We want to revert it. --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> 查看状态 </h2>

<p>首先，查看工作目录的状态。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git status</pre>

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

<p>可以看出<code>hello.html</code>文件已经被修改了，但还未添加至暂存区。</p>

<h2><em>04</em> 撤销在工作目录中的修改</h2>

<p>使用<code>checkout</code>命令可以切换回到版本库中原来的<code>hello.html</code>文件。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git checkout hello.html
git status
cat hello.html</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git checkout hello.html
$ git status
# On branch master
nothing to commit (working directory clean)
$ cat hello.html
&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>该状态消息显示在工作目录中没有还未暂存的修改。并且之前无用的注释也在hello.html文件中消失了。</p>
