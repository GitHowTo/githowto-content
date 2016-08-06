---
view: page
title: "十三、给版本打上标签"
---

<h3>目标</h3>

<ul><li>学会如何为提交对象打标签，以便于日后引用</li></ul>

<p>让我们把当前的hello程序记为版本1（v1）。</p>

<h2><em>01</em> 首次建立一个标签</h2>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git tag v1</pre>

<p>现在，这些页面的当前版本就被称为<em>v1</em>。</p>

<h2><em>02</em> 为之前版本建立标签 </h2>

<p>让我们把当前版本之前的一个版本标记为v1-beta。首先我们需要切换到前一版本。这次我们不需要再查找哈希值了，而是使用<code>^</code>符号来表示「v1的上一个版本（父版本）」。</p>

<p class="note">如果<code>v1</code>^符号产生错误，尝试使用<code>v1~1</code>指向同一版本。这个符号表示「在v1之前的第一个版本」。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git checkout v1^
cat hello.html</pre>

<h4 class="h4-pre">运行：</h4>

<pre class="sample">$ git checkout v1^
Note: checking out 'v1^'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 8c32287... Added standard HTML page tags
$ cat hello.html
&lt;html&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>这个版本具有<code>&lt;html&gt;</code>和<code>&lt;body&gt;</code>标签，但是没有<code>&lt;head&gt;</code>标签。让我们把它的版本标记为v1-beta。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git tag v1-beta</pre>

<h2><em>03</em> 使用标签名进行切换 </h2>

<p>现在尝试在两个被打上了标签的版本之间进行切换。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git checkout v1
git checkout v1-beta</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git checkout v1
Previous HEAD position was 8c32287... Added standard HTML page tags
HEAD is now at fa3c141... Added HTML header
$ git checkout v1-beta
Previous HEAD position was fa3c141... Added HTML header
HEAD is now at 8c32287... Added standard HTML page tags</pre>

<h2><em>04</em> 使用<code>tag</code>命令查看标签</h2>

<p>你可以使用<code>git tag</code>命令查看当前所有可用的标签。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git tag</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git tag
v1
v1-beta</pre>

<h2><em>05</em> 在历史记录中查看标签 </h2>

<p>你也可以在历史记录中查看标签。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git hist master --all</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git hist master --all
* fa3c141 2011-03-09 | Added HTML header (v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (HEAD, v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>你可以看到所有的标签（<code>v1</code>以及<code>v1-beta</code>）与分支名（<code>master</code>）一起出现在历史记录中。而<code>HEAD</code>则表明当前所在的提交对象（在上面的例子中则是<code>v1-beta</code>）。</p>
