---
view: page
title: "十八、删除oops标签"
---

<h3>目标</h3>

<ul><li>删除oops标签（清理工作）</li></ul>

<h2><em>01</em> oops标签的删除操作</h2>

<p>Oops标签已经完成了它的使命。让我们删除这个标签，以允许垃圾回收器清除掉被该标签引用的提交对象。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git tag -d oops
git hist --all</pre>

<h4 class="h4-pre">结果：</h4>

<pre class="sample">$ git tag -d oops
Deleted tag 'oops' (was 45fa96b)
$ git hist --all
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Oops标签已经从版本库中删除了。</p>
