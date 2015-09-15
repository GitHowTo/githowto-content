---
view: page
title: "49. Извлечение общих изменений"
---

<h3>Цели</h3>

<ul><li>Научиться извлекать изменения из общего репозитория.</li></ul>

<p>Быстро переключитесь в клонированный репозиторий и извлеките изменения, только что отправленные в общий репозиторий.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">cd ../cloned_hello</pre>

<p style="color:red;"><strong><span class="caps">Примечание</span>: Сейчас мы находимся  в репозитории <em>cloned_hello</em>.</strong></p>

<p>Продолжите с…</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git remote add shared ../hello.git
git branch --track shared master
git pull
cat README</pre>