---
view: page
title: "21. Детальніше про структуру"
---

<h3>Цілі</h3>

<ul><li>Додати ще один файл до нашого репозиторію</li></ul>

<h2><em>01</em> Додавання index.html</h2>

<p>Давайте додамо файл index.html до нашого репозиторію. Наступний файл відмінно підійде для цієї мети.</p>

<h4 class="h4-pre">Файл: <em>index.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;body&gt;
    &lt;iframe src="lib/hello.html" width="200" height="200" /&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Додайте файл і зробіть коміт.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add index.html
git commit -m "Added index.html."</pre>

<p>Тепер при відкритті index.html, ви повинні побачити шматок сторінки hello в маленькому віконці.</p>