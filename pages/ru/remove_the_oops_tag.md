---
view: page
title: "18. Удаление тега oops"
---

<h3>Цели</h3>

<ul><li>Удаление тега oops (уборка)</li></ul>

<h2><em>01</em> Удаление тега oops</h2>

<p>Тег oops свою функцию выполнил. Давайте удалим его и коммиты, на которые он ссылался, сборщиком мусора.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git tag -d oops
git hist --all</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git tag -d oops
Deleted tag 'oops' (was 45fa96b)
$ git hist --all
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Тег «oops» больше не будет отображаться в репозитории.</p>