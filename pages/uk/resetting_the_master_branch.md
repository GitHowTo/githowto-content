---
view: page
title: "33. Скидання гілки master"
---

<h3>Цілі</h3>

<ul><li>Скинути гілку master в точку до конфліктуючого коміту.</li></ul>

<h2><em>01</em> Скидання гілки master</h2>

<p>Додавши інтерактивний режим в гілку master, ми внесли зміни, конфліктуючі зі змінами в гілці style. Давайте повернемося в гілці master в точку перед внесенням конфліктуючих змін. Це дозволяє нам продемонструвати роботу команди rebase, не турбуючись про конфлікти.</p>

<h4 class="h4-pre">Виконайте:</h4>

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

<p>Коміт «Added <span class="caps">README</span>» йде безпосередньо перед комітом конфліктуючого інтерактивного режиму. Ми скинемо гілку master до коміту «Added <span class="caps">README</span>».</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git reset --hard &lt;hash&gt;
git hist --all</pre>

<p>Перегляньте лог. Він повинен виглядати так, ніби репозиторій було перемотано назад у часі до точки до будь-якого злиття.</p>

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