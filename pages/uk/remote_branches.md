---
view: page
title: "40. Віддалені гілки"
---

<h3>Цілі</h3>

<ul><li>Дізнатися про локальні і віддалені гілки</li></ul>

<p>Давайте подивимося на гілки, доступні в нашому клонованому репозиторію.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git branch</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git branch
* master</pre>

<p>Як ми бачимо, у списку лише гілка master. Де гілка style? Команда <strong>git</strong> <strong>branch</strong>, за замовчуванням, виводить лише список локальних гілок.</p>

<h2><em>01</em> Список віддалених гілок</h2>

<p>Для того, щоб побачити всі гілки, спробуйте наступну команду:</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git branch -a</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git branch -a
* master
  remotes/origin/HEAD -&gt; origin/master
  remotes/origin/style
  remotes/origin/master</pre>

<p>Git виводить всі коміти в оригінальний репозиторій, але гілки в віддаленому репозиторію не розглядаються як локальні. Якщо ми хочемо власну гілку <strong>style</strong>, ми повинні самі її створити. Через хвилину ви побачите, як це робиться</p>