---
view: page
title: "九、是修改，而不是文件"
---

<h3>目标</h3>

<ul><li>理解git的操作对象是修改，而不是文件。</li></ul>

<p>绝大多数的版本控制系统的操作对象是文件。你将文件添加至版本控制系统，它将跟踪记录从那时起的所有修改。</p>

<p>而Git则聚焦于对一个文件的修改，而不是文件本身。一条<code>git add file</code>命令并不是让git将该文件添加至版本库，而是让它注意当前的文件状态，以便后续的提交。</p>

<p>在这一课中，我们将会尝试体会这两种区别。</p>

<h2><em>01</em> 第一次修改：添加默认页面标签</h2>

<p>修改『Hello, World』页面，使其包含默认的<code>html</code>和<code>body</code>标签。</p>

<h4 class="h4-pre">文件：<em>hello.html</em></h4>

<pre class="file"><strong>&lt;html&gt;
  &lt;body&gt;</strong>
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  <strong>&lt;/body&gt;
&lt;/html&gt;</strong></pre>

<h2><em>02</em> 添加本次修改</h2>

<p>现在把本次修改添加至git暂存区</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>03</em> 第二次修改：添加HTML头部信息</h2>

<p>现在将HTML头部信息（<code>head</code>区）添加到『Hello, World』页面。</p>

<h4 class="h4-pre">文件：<em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>04</em> 查看当前（版本库的）状态</h2>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git status</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#</pre>

<p>需要注意的是hello.html文件在以上的状态信息中出现了两次。第一次修改（添加默认标签）已经被暂存并随时可以提交了。而第二次修改（添加HTML头信息）还未被暂存。如果现在就直接进行提交操作，HTML头信息将不会被保存到版本库中。</p>

<p>让我们试一下，看看是否真的如此。</p>

<h2><em>05</em> 提交</h2>

<p>提交已经暂存的修改（默认标签），然后再次查看状态。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git commit -m "Added standard HTML page tags"
git status</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git commit -m "Added standard HTML page tags"
[master 8c32287] Added standard HTML page tags
 1 files changed, 3 insertions(+), 1 deletions(-)
$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>状态查看命令显示<code>hello.html</code>文件存在未被记录的修改，但这些修改已经不在缓冲区了。</p>

<h2><em>06</em> 添加第二次修改</h2>

<p>将第二次修改添加至暂存区，然后再运行<code>git status</code>命令。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git add .
git status</pre>

<p class="note"><strong>注：</strong>在以上命令中，当前目录（「.」）作为被添加的文件。这是一种快捷方式，它将当前目录及其子目录中所有发生修改的文件一次性全部添加到暂存区。但正是因为它会添加所有被修改的文件，因此最好在运行<tt>add .</tt>之前查看一下版本库状态，这样可以避免过早地添加那些还不需要被添加的文件。</p>

<p class="note">我想让你先接触『add .』技巧，后续我们还将继续使用它。</p>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>第二次的修改已经被暂存并随时可以进行提交了。</p>

<h2><em>07</em> 提交第二次修改</h2>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git commit -m "Added HTML header"</pre>
