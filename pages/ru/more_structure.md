---
view: page
title: "21. Подробнее о структуре"
---

<h3>Цели</h3>

<ul><li>Добавить еще один файл в наш репозиторий</li></ul>

<h2><em>01</em> Добавление index.html</h2>

<p>Давайте добавим файл index.html в наш репозиторий. Следующий файл отлично подойдет для этой цели.</p>

<h4 class="h4-pre">Файл: <em>index.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;body&gt;
    &lt;iframe src="lib/hello.html" width="200" height="200" /&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Добавьте файл и сделайте коммит.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add index.html
git commit -m "Added index.html."</pre>

<p>Теперь при открытии index.html, вы должны увидеть кусок страницы hello в маленьком окошке.</p>