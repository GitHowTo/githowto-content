---
view: page
title: "30. Вирішення конфліктів"
---

<h3>Цілі</h3>

<ul><li>Навчитися вирішувати конфлікти під час злиття</li></ul>

<h2><em>01</em> Злиття master з гілкою style</h2>

<p>Тепер повернемося до гілки style і спробуємо об'єднати її з новою гілкою  master.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout style
git merge master</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ git merge master
Auto-merging lib/hello.html
CONFLICT (content): Merge conflict in lib/hello.html
Automatic merge failed; fix conflicts and then commit the result.</pre>

<p>Якщо ви відкриєте lib/hello.html, ви побачите:</p>

<h4 class="h4-pre">Файл: <em>lib/hello.html</em></h4>

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

<p>Перший розділ - версія на чолі поточної гілки (style). Другий розділ - версія гілки  master.</p>

<h2><em>02</em> Рішення конфлікту</h2>

<p>Вам необхідно вручну вирішити конфлікт. Внесіть зміни в  <code>lib/hello.html</code> для досягнення наступного результату.</p>

<h4 class="h4-pre">Файл: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World! Life is great!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Зробіть коміт вирішення конфлікту</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m "Merged master fixed conflict."</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git add lib/hello.html
$ git commit -m "Merged master fixed conflict."
Recorded resolution for 'lib/hello.html'.
[style 645c4e6] Merged master fixed conflict.</pre>

<h2><em>04</em> Розширені можливості злиття</h2>

<p>Git не надає ніяких графічних інструментів злиття, але буде із задоволенням працювати з будь-якими сторонніми інструментами злиття, які ви хочете використовувати (<a href="http://stackoverflow.com/questions/137102/whats-the-best-visual-merge-tool-for-git">обговорення таких інструментів на StackOverflow</a>).</p>