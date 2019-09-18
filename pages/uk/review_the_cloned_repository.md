---
view: page
title: "38. Перегляд клонованого репозиторію"
---

<h3>Цілі</h3>

<ul><li>Дізнатися про гілки у віддалених репозиторіях.</li></ul>

<h2><em>01</em> Подивіться на клонований репозиторій</h2>

<p>Давайте поглянемо на клонований репозиторій.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cd cloned_hello
ls</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cd cloned_hello
$ ls
README
index.html
lib</pre>

<p>Ви побачите список всіх файлів на верхньому рівні оригінального репозиторію (<code>README</code>, <code>index.html</code> і <code>lib</code>).</p>

<h2><em>02</em> Перегляньте історію репозиторію</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist --all
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, origin/master, origin/style, origin/HEAD, master) [Alexander Shvets]
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

<p>Ви побачите список всіх комітів у новий репозиторій, і він повинен (більш-менш) збігатися з історією комітів в оригінальному репозиторію. Єдина різниця повинна бути в назвах гілок.</p>

<h2><em>03</em> Віддалені гілки</h2>

<p>Ви побачите гілку <strong>master</strong> (<strong><span class="caps">HEAD</span></strong>) в списку історії. Ви також побачите гілки з дивними іменами (<strong>origin/master</strong>, <strong>origin/style</strong> і <strong>origin/<span class="caps">HEAD</span></strong>). Ми поговоримо про них трохи пізніше.</p>