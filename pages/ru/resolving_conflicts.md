---
view: page
title: "30. Разрешение конфликтов"
---

<h3>Цели</h3>

<ul><li>Научиться разрешать конфликты во время слияния</li></ul>

<h2><em>01</em> Слияние master с веткой style</h2>

<p>Теперь вернемся к ветке style и попытаемся объединить ее с новой веткой master.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout style
git merge master</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ git merge master
Auto-merging lib/hello.html
CONFLICT (content): Merge conflict in lib/hello.html
Automatic merge failed; fix conflicts and then commit the result.</pre>

<p>Если вы откроете lib/hello.html, вы увидите:</p>

<h4 class="h4-pre">Файл: <em style="text-transform: none">lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
&lt;&lt;&lt;&lt;&lt;&lt;&lt; HEAD
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
=======
    &lt;!-- no style --&gt;
&gt;&gt;&gt;&gt;&gt;&gt;&gt; master
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello,World! Life is great!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

<p>Первый раздел - версия во главе текущей ветки (style). Второй раздел - версия ветки master.</p>

<h2><em>02</em> Решение конфликта</h2>

<p>Вам необходимо вручную разрешить конфликт. Внесите изменения в  <code>lib/hello.html</code> для достижения следующего результата.</p>

<h4 class="h4-pre">Файл: <em style="text-transform: none">lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World! Life is great!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Сделайте коммит решения конфликта</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m "Merged master fixed conflict."</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git add lib/hello.html
$ git commit -m "Merged master fixed conflict."
Recorded resolution for 'lib/hello.html'.
[style 645c4e6] Merged master fixed conflict.</pre>

<h2><em>04</em> Расширенные возможности слияния</h2>

<p>Git не предоставляет никаких графических инструментов слияния, но будет с удовольствием работать с любыми сторонними инструментами слияния, которые вы хотите использовать (<a href="http://stackoverflow.com/questions/137102/whats-the-best-visual-merge-tool-for-git">обсуждение таких инструментов на StackOverflow</a>).</p>
