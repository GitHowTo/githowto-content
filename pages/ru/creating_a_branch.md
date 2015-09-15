---
view: page
title: "24. Создание ветки"
---

<h3>Цели</h3>

<ul><li>Научиться создавать локальную ветку в репозитории</li></ul>

<p>Пора сделать наш hello world более выразительным. Так как это может занять некоторое время, лучше переместить эти изменения в отдельную ветку, чтобы изолировать их от изменений в ветке master.</p>

<h2><em>01</em> Создайте ветку</h2>

<p>Давайте назовем нашу новую ветку «style».</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout -b style
git status</pre>

<p class="note"><strong><span class="caps">Примечание</span>: </strong><code>git checkout -b &lt;имяветки&gt;</code> является шорткатом для <code>git branch &lt;имяветки&gt;</code> за которым идет <code>git checkout &lt;имяветки&gt;</code>.</p>

<p>Обратите внимание, что команда <code>git status</code> сообщает о том, что вы находитесь в ветке «style».</p>

<h2><em>02</em>Добавьте файл стилей style.css</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">touch lib/style.css</pre>

<h4 class="h4-pre">Файл: <em>lib/style.css</em></h4>

<pre class="file">h1 {
  color: red;
}</pre>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add lib/style.css
git commit -m "Added css stylesheet"</pre>

<h2><em>03</em>Измените основную страницу</h2>

<p>Обновите файл hello.html, чтобы использовать стили style.css.</p>

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

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m "Hello uses style.css"</pre>

<h2><em>04</em>Измените index.html</h2>

<p>Обновите файл index.html, чтобы он тоже использовал style.css</p>

<h4 class="h4-pre">Файл: <em>index.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="lib/style.css" /&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;iframe src="lib/hello.html" width="200" height="200" /&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add index.html
git commit -m "Updated index.html"</pre>

<h2><em>05</em> Далее</h2>

<p>Теперь у нас есть новая ветка под названием <strong>style</strong> с 3 новыми коммитами. Далее мы узнаем, как осуществлять навигацию и переключаться между ветками.</p>