---
view: page
title: "27. Просмотр отличающихся веток"
---

<h3>Цели</h3>

<ul><li>Научиться просматривать отличающиеся ветки в репозитории.</li></ul>

<h2><em>01</em> Просмотрите текущие ветки</h2>

<p>Теперь у нас в репозитории есть две отличающиеся ветки. Используйте следующую лог-команду для просмотра веток и их отличий.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist --all
* 6c0f848 2011-03-09 | Added README (HEAD, master) [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html (style) [Alexander Shvets]
| * 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
| * 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Это наша первая возможность увидеть в действии <code>--graph</code> в <code>git hist</code>. Добавление опции <code>--graph</code> в <code>git log</code> вызывает построение дерева коммитов с помощью простых <span class="caps">ASCII</span> символов. Мы видим обе ветки (style и master), и то, что ветка master является текущей <span class="caps">HEAD</span>. Общим предшественником обеих веток является ветка «Added index.html».</p>

<p>Метка <code>--all</code> гарантированно означает, что мы видим все ветки. По умолчанию показывается только текущая ветка.</p>