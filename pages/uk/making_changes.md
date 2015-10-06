---
view: page
title: "5. Внесення змін"
---

<h3>Цілі</h3>

<ul><li>Навчитися відслідковувати стан робочого каталогу</li></ul>

<h2><em>01</em> Змініть сторінку «Hello, World»</h2>

<p>Додамо деякі HTML-теги до нашого вітання. Змініть вміст файлу на:</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;h1&gt;</strong>Hello, World!<strong>&lt;/h1&gt;</strong></pre>

<h2><em>02</em> Перевірте стан</h2>

<p>Зараз перевірте стан робочого каталогу.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git status</pre>

<p>Ви побачите…</p>

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

<p>Перше, що потрібно зауважити, це те, що git знає, що файл <code>hello.html</code> було змінено, але ці зміни ще не зафіксовано у репозиторію.</p>

<p>Також, зверніть увагу, що повідомлення про стан репозитарію дає вам підказку про те, що необхідно зробити далі. Якщо ви хочете внести зміни у репозиторій, скористайтеся командою <code>git add</code>. Якщо ні - виконайте команду <code>git сheckout</code> для скасування змін.</p>

<h2><em>03</em> А далі...</h2>

<p>Давайте проіндексуемо зміни.</p>
