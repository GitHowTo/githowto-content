---
view: page
title: "42. Витяг змін"
---

<h3>Цілі</h3>

<ul><li>Навчитися витягувати зміни з віддаленого репозиторію.</li></ul>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cd ../cloned_hello
git fetch
git hist --all</pre>

<p style="color:red;"><strong><span class="caps">Примітка</span>: Зараз ми знаходимося в репозиторію <em>cloned_hello</em> </strong></p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git fetch
From /Users/alex/Documents/Presentations/githowto/auto/hello
   6e6c76a..2faa4ea  master     -&gt; origin/master
$ git hist --all
* 2faa4ea 2011-03-09 | Changed README in original repo (origin/master, origin/HEAD) [Alexander Shvets]
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, origin/style, master) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>На даний момент в репозиторію є всі коміти з оригінального репозиторію, але вони не інтегровані в локальні гілки клонованого репозиторію.</p>

<p>В історії вище знайдіть коміт «Changed <span class="caps">README</span> in original repo». Зверніть увагу, що коміт містить у собі коміти «origin/master» и «origin/<span class="caps">HEAD</span>».</p>

<p>Тепер давайте подивимося на коміт «Updated index.html». Ви побачите, що локальна гілка master вказує на цей коміт, а не на новий коміт, котрий ми щойно витягли.</p>

<p>Висновком є ​​те, що команда «git fetch» ​​буде витягувати нові коміти з віддаленого репозиторію, але не буде зливати їх з вашими напрацюваннями в локальних гілках.</p>

<h2><em>01</em> Перевірте <span class="caps">README</span></h2>

<p>Ми можемо продемонструвати, що клонований файл <span class="caps">README</span> не змінився.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cat README</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.</pre>

<p>Як бачите, ніяких змін.</p>