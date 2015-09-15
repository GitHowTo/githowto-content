---
view: page
title: "23. Git внутри: Работа непосредственно с объектами git"
---

<h3>Цели</h3>

<ul><li>Исследовать структуру базы данных объектов</li>
<li>Научиться использовать SHA1 хэши для поиска содержимого в репозитории</li></ul>

<p>Давайте исследуем объекты git с помощью некоторых инструментов.</p>

<h2><em>01</em> Поиск последнего коммита</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist --max-count=1</pre>

<p>Эта команда должна показать последний коммит в репозиторий. SHA1 хэш в вашей системе, вероятно, отличается от моего, но вы увидите что-то наподобие этого.</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist --max-count=1
* 8029c07 2011-03-09 | Added index.html. (HEAD, master) [Alexander Shvets]</pre>

<h2><em>02</em> Вывод последнего коммита</h2>

<p>С помощью SHA1 хэша из коммита,  указанного выше…</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git cat-file -t &lt;hash&gt;
git cat-file -p &lt;hash&gt;</pre>

<p>Вот что выходит у меня…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git cat-file -t 8029c07
commit
$ git cat-file -p 8029c07
tree 096b74c56bfc6b40e754fc0725b8c70b2038b91e
parent 567948ac55daa723807c0c16e34c76797efbcbed
author Alexander Shvets &lt;alex@githowto.com&gt; 1299684476 -0500
committer Alexander Shvets &lt;alex@githowto.com&gt; 1299684476 -0500

Added index.html.</pre>

<p class="note"><strong><span class="caps">Примечание</span>:</strong> Если вы задали алиасы «type» и «dump», как описано в <a href="aliases">уроке об алиасах</a>, можете вводить команды <code>git type</code> и <code>git dump</code> вместо длинных команд (которые я никогда не запоминаю).</p>

<p>Это вывод объекта коммита, который находится во главе ветки master.</p>

<h2><em>03</em> Поиск дерева</h2>

<p>Мы можем вывести дерево каталогов, ссылка на который идет в коммите. Это должно быть описание файлов (верхнего уровня) в нашем проекте (для конкретного коммита). Используйте SHA1 хэш из строки «дерева», из списка выше.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git cat-file -p &lt;treehash&gt;</pre>

<p>Вот как выглядит мое дерево…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git cat-file -p 096b74c
100644 blob 28e0e9d6ea7e25f35ec64a43f569b550e8386f90	index.html
040000 tree e46f374f5b36c6f02fb3e9e922b79044f754d795	lib</pre>

<p>Да, я вижу index.html и каталог lib.</p>

<h2><em>04</em> Вывод каталога lib</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git cat-file -p &lt;libhash&gt;</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git cat-file -p e46f374
100644 blob c45f26b6fdc7db6ba779fc4c385d9d24fc12cf72	hello.html</pre>

<p>Существует файл <code>hello.html</code>.</p>

<h2><em>05</em> Вывод файла <code>hello.html</code></h2>

<h4 class="h4-pre">Выполните:</h4>

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

<p>А вот и он. Мы вывели объекты коммитов, объекты деревьев и объекты блобов непосредственно из репозитория git. Это все, что есть – блобы, деревья и коммиты.</p>

<h2><em>06</em> Исследуйте самостоятельно</h2>

<p>Исследуйте git репозиторий вручную самостоятельно. Смотрите, удастся ли вам найти оригинальный файл hello.html с самого первого коммита вручную по ссылкам SHA1 хэша в последнем коммите.</p>