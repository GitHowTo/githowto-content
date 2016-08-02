---
view: page
title: "八、提交修改内容"
---

<h3>目标</h3>

<ul><li>学会将修改提交至版本库中</li></ul>

<h2><em>01</em> 提交修改 </h2>

<p>关于暂存的讨论先告一段落，让我们将暂存的修改提交到版本库中去。</p>

<p>在你之前使用<code>git commit</code>将<code>hello.html</code>的第一版提交到版本库的时候，还附带了一个<code>-m</code>参数，它的作用是包含一句关于本次提交的注释。除此之外，提交命令也允许交互式地编辑提交注释。现在让我们看看这种功能如何使用。</p>

<p>如果你在命令行中省略掉<code>-m</code>参数，git将会使你进入到一个文本编辑器中，该文本编辑器的选择依据是以下的设置（按照次序优先级）：</p>

<ul>
<li>GIT_EDITOR 环境变量</li>
<li>core.editor 配置文件中的设置</li>
<li><span class="caps">VISUAL</span> 环境变量</li>
<li><span class="caps">EDITOR</span> 环境变量</li>
</ul>

<p>本教程中只将<span class="caps">EDITOR</span>环境变量设置成为<code>emacsclient</code>（在Linux与Mac中可用）。</p>

<p>Let us commit now and check the status.</p>
<p>现在让我们来进行提交并查看状态。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git commit</pre>

<p>你将会在你的文本编辑器中看到以下内容：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">|
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>在第一行中输入如下注释："Added <span class="caps">hi tag</span>"。保存文件并退出编辑器（在默认的VIM编辑器中，先按ESC建，再输入<code>:wq</code>命令，再按回车键。）你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">git commit
Waiting for Emacs...
[master 569aa96] Added h1 tag
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>"Waiting for Emacs&#8230;"是获取自<code>emacsclient</code>程序，它将文件发送至一个运行的emacs程序并等待处理结束。其余的数据是标准的提交消息。</p>

<h2><em>02</em> 查看状态</h2>

<p>最后让我们查看一下当前的状态。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git status</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>工作目录处于干净的状态，你可以继续进行工作。</p>
