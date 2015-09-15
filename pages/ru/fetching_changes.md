---
view: page
title: "42. Извлечение изменений"
---

<h3>Цели</h3>

<ul><li>Научиться извлекать изменения из удаленного репозитория.</li></ul>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">cd ../cloned_hello
git fetch
git hist --all</pre>

<p style="color:red;"><strong><span class="caps">Примечание</span>: Сейчас мы находимся  в репозитории <em>cloned_hello</em> </strong></p>

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

<p>На данный момент в репозитории есть все коммиты из оригинального репозитория, но они не интегрированы в локальные ветки клонированного репозитория.</p>

<p>В истории выше найдите коммит «Changed <span class="caps">README</span> in original repo». Обратите внимание, что коммит включает в себя коммиты «origin/master» и «origin/<span class="caps">HEAD</span>».</p>

<p>Теперь  давайте посмотрим на коммит «Updated index.html». Вы увидите, что локальная ветка master указывает на этот коммит, а не на новый коммит, который мы только что извлекли.</p>

<p>Выводом является то, что команда «git fetch» будет извлекать новые коммиты из удаленного репозитория, но не будет сливать их с вашими наработками в локальных ветках.</p>

<h2><em>01</em> Проверьте <span class="caps">README</span></h2>

<p>Мы можем продемонстрировать, что клонированный файл <span class="caps">README</span> не изменился.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">cat README</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.</pre>

<p>Как видите, никаких изменений.</p>