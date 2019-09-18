---
view: page
title: "20. Перемещение файлов"
---

<h3>Цели</h3>

<ul><li>Научиться перемещать файл в пределах репозитория.</li></ul>

<h2><em>01</em> Переместите файл hello.html в каталог lib</h2>

<p>Сейчас мы собираемся создать структуру нашего репозитория. Давайте перенесем страницу в каталог lib.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">mkdir lib
git mv hello.html lib
git status</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ mkdir lib
$ git mv hello.html lib
$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	renamed:    hello.html -&gt; lib/hello.html
#</pre>

<p>Перемещая файлы с помощью git, мы информируем git о 2 вещах</p>

<ol>
<li>Что файл <code>hello.html</code> был удален.</li>
<li>Что файл <code>lib/hello.html</code> был создан.</li>
</ol>
<p>Оба эти факта сразу же проиндексированы и готовы к коммиту. Команда git status сообщает, что файл был перемещен.</p>

<h2><em>02</em> Второй способ перемещения файлов</h2>

<p>Позитивной чертой git является то, что вы можете забыть о версионном контроле до того момента, когда вы готовы приступить к коммиту кода. Что бы случилось, если бы мы использовали командную строку операционной системы для перемещения файлов вместо команды git?</p>

<p>Оказывается, следующий набор команд идентичен нашим последним действиям. Работы здесь побольше, но результат тот же.</p>

<p class="command"> Мы могли бы выполнить:</p>

<pre class="instructions">mkdir lib
mv hello.html lib
git add lib/hello.html
git rm hello.html</pre>

<h2><em>03</em> Коммит в новый каталог</h2>

<p>Давайте сделаем коммит этого перемещения.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git commit -m "Moved hello.html to lib"</pre>