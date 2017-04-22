---
view: page
title: "49. Витяг загальних змін"
---

<h3>Цілі</h3>

<ul><li>Навчитися отримувати зміни із загального репозиторію.</li></ul>

<p>Швидко переключіться в клонований репозиторій і витягніть зміни, щойно відправлені в загальний репозиторій.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cd ../cloned_hello</pre>

<p style="color:red;"><strong><span class="caps">Примітка</span>: Зараз ми знаходимося у репозиторію <em>cloned_hello</em>.</strong></p>

<p>Продовжіть з…</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git remote add shared ../hello.git
git branch --track shared master
git pull shared master
cat README</pre>
