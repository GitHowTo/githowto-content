---
view: page
title: "33. Сброс ветки master"
---

<h3>Цели</h3>

<ul><li>Сбросить ветку master в точку до конфликтующего коммита.</li></ul>

<h2><em>01</em> Сброс ветки master</h2>

<p>Добавив интерактивный режим в ветку master, мы внесли изменения, конфликтующие с изменениями в ветке style. Давайте вернемся в ветке master в точку перед внесением конфликтующих изменений. Это позволяет нам продемонстрировать работу команды rebase, не беспокоясь о конфликтах.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout master
git hist</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist
* 454ec68 2011-03-09 | Life is great! (HEAD, master) [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Коммит «Added <span class="caps">README</span>» идет непосредственно перед коммитом конфликтующего интерактивного режима. Мы сбросим ветку master к коммиту «Added <span class="caps">README</span>».</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git reset --hard &lt;hash&gt;
git hist --all</pre>

<p>Просмотрите лог. Он должен выглядеть, как будто  репозиторий был перемотан назад во времени к точке до какого-либо слияния.</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git reset --hard 6c0f848
$ git hist --all
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