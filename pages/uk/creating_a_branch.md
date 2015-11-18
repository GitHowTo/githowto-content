---
view: page
title: "24. Створення гілки"
---

<h3>Цілі</h3>

<ul><li>Навчитися створювати локальну гілку в репозиторію</li></ul>

<p>Пора зробити наш hello world виразнішим. Так як це може зайняти деякий час, краще перемістити ці зміни в окрему гілку, щоб ізолювати їх від змін в гілці master.</p>

<h2><em>01</em> Створіть гілку</h2>

<p>Давайте назвемо нашу нову гілку «style».</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout -b style
git status</pre>

<p class="note"><strong><span class="caps">Примітка</span>: </strong><code>git checkout -b &lt;им'ягілки&gt;</code> є шорткатом для <code>git branch &lt;им'ягілки&gt;</code> за котрим йде <code>git checkout &lt;им'ягілки&gt;</code>.</p>

<p>Зверніть увагу, що команда <code>git status</code> повідомляє про те, що ви перебуваєте в гілці «style».</p>

<h2><em>02</em>Додайте файл стилів style.css</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">touch lib/style.css</pre>

<h4 class="h4-pre">Файл: <em>lib/style.css</em></h4>

<pre class="file">h1 {
  color: red;
}</pre>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add lib/style.css
git commit -m "Added css stylesheet"</pre>

<h2><em>03</em>Змініть основну сторінку</h2>

<p>Оновіть файл hello.html, щоб використовувати стилі style.css.</p>

<h4 class="h4-pre">Файл: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
<strong>    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m "Hello uses style.css"</pre>

<h2><em>04</em>Змініть index.html</h2>

<p>Оновіть файл index.html, щоб він теж використовував style.css</p>

<h4 class="h4-pre">Файл: <em>index.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="lib/style.css" /&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;iframe src="lib/hello.html" width="200" height="200" /&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add index.html
git commit -m "Updated index.html"</pre>

<h2><em>05</em> Далі</h2>

<p>Тепер у нас є нова гілка під назвою <strong>style</strong> з 3-ма новими комітами. Далі ми дізнаємось, як здійснювати навігацію і перемикатися між гілками.</p>