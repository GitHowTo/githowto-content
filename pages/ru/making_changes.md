---
view: page
title: "5. Внесение изменений"
---

<h3>Цели</h3>

<ul><li>Научиться отслеживать состояние рабочего каталога</li></ul>

<h2><em>01</em> Измените страницу «Hello, World»</h2>

<p>Добавим кое-какие HTML-теги к нашему приветствию. Измените содержимое файла на:</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;h1&gt;</strong>Hello, World!<strong>&lt;/h1&gt;</strong></pre>

<h2><em>02</em> Проверьте состояние</h2>

<p>Теперь проверьте состояние рабочего каталога.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git status</pre>

<p>Вы увидите …</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>Первое, что нужно заметить, это то, что git знает, что файл <code>hello.html</code> был изменен, но при этом эти изменения еще не зафиксированы в репозитории.</p>

<p>Также обратите внимание на то, что сообщение о состоянии дает вам подсказку о том, что нужно делать дальше. Если вы хотите добавить эти изменения в репозиторий, используйте команду <code>git add</code>. В противном случае используйте команду <code>git сheckout</code> для отмены изменений.</p>

<h2><em>03</em> А далее...</h2>

<p>Давайте проиндексируем изменения.</p>