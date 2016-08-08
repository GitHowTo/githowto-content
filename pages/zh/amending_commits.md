---
view: page
title: "十九、修改提交对象"
---

<h3>目标</h3>

<ul><li>学会如何修改一个已经存在的提交对象</li></ul>

<h2><em>01</em> 修改页面并提交</h2>

<p>在页面上添加一项作者注释。</p>

<h4 class="h4-pre">文件：<em>hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git add hello.html
git commit -m "Add an author comment"</pre>

<h2><em>02</em> 啊哦，忘记电子邮件了</h2>

<p>在提交之后你想起每个优秀的注释都应该包括作者的邮箱。接下来更新hello页面，添加邮箱信息。</p>

<h4 class="h4-pre">文件：<em>hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> 修改前一次提交对象</h2>

<p>我们并不想为添加邮箱的修改创建一个新的提交对象。让我们直接修改前一次提交对象来完成添加邮箱的修改。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git add hello.html
git commit --amend -m "Add an author/email comment"</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git add hello.html
$ git commit --amend -m "Add an author/email comment"
[master 6a78635] Add an author/email comment
 1 files changed, 2 insertions(+), 1 deletions(-)</pre>

<h2><em>04</em> 查看历史</h2>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git hist
* 6a78635 2011-03-09 | Add an author/email comment (HEAD, master) [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>可以看到，新的『author/email』的提交已经取代了原来的『author』提交对象。而同样的效果也可以通过先重置分支中的上一次提交，然后再重新提交一次新的修改来完成。</p>
