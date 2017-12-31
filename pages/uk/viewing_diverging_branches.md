---
view: page
title: "27. Перегляд розбіжних гілок"
---

<h3>Цілі</h3>

<ul><li>Навчитися переглядати розбіжні гілки у репозиторію.</li></ul>

<h2><em>01</em> Перегляньте поточні гілки</h2>

<p>Тепер у нас в репозиторію є дві відмінні гілки. Використовуйте наступну лог-команду для перегляду гілок і їх відмінностей.</p>

<h4 class="h4-pre">Виконайте:</h4>

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

<p>Це наша перша можливість побачити в дії <code>--graph</code> в <code>git hist</code>. Додавання опції <code>--graph</code> в <code>git log</code> викликає побудову дерева комітів за допомогою простих <span class="caps">ASCII</span> символів. Ми бачимо обидві гілки (style і master), і те, що гілка master є поточною <span class="caps">HEAD</span>. Загальним попередником обох гілок є гілка «Added index.html».</p>

<p>Мітка <code>--all</code> гарантує, що ми бачимо всі гілки. За замовчуванням показується лише поточна гілка.</p>
