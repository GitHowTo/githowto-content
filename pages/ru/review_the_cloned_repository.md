---
view: page
title: "38. Просмотр клонированного репозитория"
---

<h3>Цели</h3>

<ul><li>Узнать о ветках в удаленных репозиториях.</li></ul>

<h2><em>01</em> Посмотрите на клонированный репозиторий</h2>

<p>Давайте взглянем на клонированный репозиторий.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">cd cloned_hello
ls</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cd cloned_hello
$ ls
README
index.html
lib</pre>

<p>Вы увидите список всех файлов на верхнем уровне оригинального репозитория <code>README</code>, <code>index.html</code> и <code>lib</code>).</p>

<h2><em>02</em> Просмотрите историю репозитория</h2>

<h4 class="h4-pre">Выполните:</h4>

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

<p>Вы увидите список всех коммитов в новом репозитории, и он должен (более или менее) совпадать с историей коммитов в оригинальном репозитории. Единственная разница должна быть в названиях веток.</p>

<h2><em>03</em> Удаленные ветки</h2>

<p>Вы увидите ветку <strong>master</strong> (<strong><span class="caps">HEAD</span></strong>) в списке истории. Вы также увидите ветки со странными именами (<strong>origin/master</strong>, <strong>origin/style</strong> и <strong>origin/<span class="caps">HEAD</span></strong>). Мы поговорим о них чуть позже.</p>
