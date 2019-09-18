---
view: page
title: "23. Git всередині: Робота безпосередньо з об'єктами git"
---

<h3>Цілі</h3>

<ul><li>Дослідити структуру бази даних об'єктів</li>
<li>Навчитися використовувати SHA1 хеши для пошуку вмісту в репозиторії</li></ul>

<p>Давайте дослідимо об'єкти git за допомогою деяких інструментів.</p>

<h2><em>01</em> Пошук останнього коміту</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git hist --max-count=1</pre>

<p>Ця команда повинна показати останній коміт у репозиторію. SHA1 хеш у вашій системі, ймовірно, відрізняється від мого, але ви побачите щось на зразок цього.</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist --max-count=1
* 8029c07 2011-03-09 | Added index.html. (HEAD, master) [Alexander Shvets]</pre>

<h2><em>02</em> Вивід останнього коміту</h2>

<p>За допомогою SHA1 хешу з коміту, зазначеного вище…</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git cat-file -t &lt;hash&gt;
git cat-file -p &lt;hash&gt;</pre>

<p>Ось що виходить у мене…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git cat-file -t 8029c07
commit
$ git cat-file -p 8029c07
tree 096b74c56bfc6b40e754fc0725b8c70b2038b91e
parent 567948ac55daa723807c0c16e34c76797efbcbed
author Alexander Shvets &lt;alex@githowto.com&gt; 1299684476 -0500
committer Alexander Shvets &lt;alex@githowto.com&gt; 1299684476 -0500

Added index.html.</pre>

<p class="note"><strong><span class="caps">Примітка</span>:</strong> Якщо ви задали аліаси «type» і «dump», як описано в <a href="aliases">уроці про аліаси</a>, можете вводити команди <code>git type</code> і <code>git dump</code> замість довгих команд (які я ніколи не запам'ятовую).</p>

<p>Це вивід об'єкта коміту, який знаходиться на чолі гілки master.</p>

<h2><em>03</em> Пошук дерева</h2>

<p>Ми можемо вивести дерево каталогів, посилання на який йде в коміті. Це має бути опис файлів (верхнього рівня) в нашому проекті (для конкретного коміту). Використовуйте SHA1 хеш з рядка «дерева», зі списку вище.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git cat-file -p &lt;treehash&gt;</pre>

<p>Ось як виглядає моє дерево…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git cat-file -p 096b74c
100644 blob 28e0e9d6ea7e25f35ec64a43f569b550e8386f90	index.html
040000 tree e46f374f5b36c6f02fb3e9e922b79044f754d795	lib</pre>

<p>Так, я бачу index.html і каталог lib.</p>

<h2><em>04</em> Вивід каталогу lib</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git cat-file -p &lt;libhash&gt;</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git cat-file -p e46f374
100644 blob c45f26b6fdc7db6ba779fc4c385d9d24fc12cf72	hello.html</pre>

<p>Існує файл <code>hello.html</code>.</p>

<h2><em>05</em> Вивід файлу <code>hello.html</code></h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git cat-file -p &lt;hellohash&gt;</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git cat-file -p c45f26b
&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>А ось і він. Ми вивели об'єкти комітів, об'єкти дерев і об'єкти блобів безпосередньо з репозиторію  git. Це все, що є – блоби, дерева і коміти.</p>

<h2><em>06</em> Дослідіть самостійно</h2>

<p>Дослідіть git репозиторій вручну самостійно. Дивіться, чи вдасться вам знайти оригінальний файл hello.html з найпершого коміту вручну по посиланнях SHA1 хеша в останньому коміті</p>