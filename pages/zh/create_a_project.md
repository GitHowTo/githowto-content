---
view: page
title: "三、创建一个项目"
---

<h3>目标</h3>

<ul><li>学习如何从头开始创建一个git版本库</li></ul>

<h2><em>01</em> 创建一个『Hello, World』（『你好，世界』）页面</h2>

<p>首先进入到一个空的工作目录下（例如，在前一课中下载的压缩文件中的Work目录），创建一个空目录并命名为『hello』，然后在该目录下创建一个名为<code>hello.html</code>的文件，在其中写入下面的内容。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">mkdir hello
cd hello
touch hello.html</pre>

<h4 class="h4-pre">文件: <em>hello.html</em></h4>

<pre class="file">Hello, World</pre>

<h2><em>02</em> 创建一个版本库</h2>

<p>现在你已经有了一个包含有一个文件的目录，运行git init命令就可以在该目录中创建一个git版本库。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git init</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git init
Initialized empty Git repository in /Users/alex/Documents/Presentations/githowto/auto/hello/.git/
</pre>

<h2><em>03</em> 在版本库中添加一个页面</h2>

<p>现在让我们将刚才的『Hello, World』页面添加到版本库中。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git add hello.html
git commit -m "First Commit"</pre>

<p>你将会看到：</p>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git add hello.html
$ git commit -m "First Commit"
[master (root-commit) 911e8c9] First Commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 hello.html</pre>
