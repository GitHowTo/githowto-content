---
view: page
title: "六、暂存修改"
---

<h3>目标</h3>

<ul><li>学会暂存修改，为接下来的提交操作做好准备</li></ul>

<h2><em>01</em> 添加修改</h2>

<p>现在使用git暂存修改。并检查状态</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git add hello.html
git status</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git add hello.html
$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>hello.html文件上发生的修改已经被暂存了。这表明git知道相关的修改，但是这些修改还不存在于版本库中。接下来的提交操作将会包含暂存的修改。</p>

<p>如果你决定不提交本次修改，以上的状态消息提示你可以使用<code>git reset</code>命令撤销之前暂存的修改。</p>
