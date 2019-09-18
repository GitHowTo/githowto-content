---
view: page
title: "20. Переміщення файлів"
---

<h3>Цілі</h3>

<ul><li>Навчитися переміщати файл в межах репозиторію.</li></ul>

<h2><em>01</em> Перемістіть файл hello.html в каталог lib</h2>

<p>Зараз ми збираємося змінити структуру нашого репозиторію. Давайте перенесемо сторінку в каталог lib.</p>

<h4 class="h4-pre">Виконайте:</h4>

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

<p>Переміщуючи файли за допомогою git, ми інформуємо git про 2 речі</p>

<ol>
<li>Що файл <code>hello.html</code> було видалено.</li>
<li>Що файл <code>lib/hello.html</code> було створено.</li>
</ol>
<p>Обидва ці факти відразу ж проіндексовані і готові до коміту. Команда git status повідомляє, що файл був переміщений.</p>

<h2><em>02</em> Другий спосіб переміщення файлів</h2>

<p>Позитивною рисою git є те, що ви можете забути про версійний контроль до того часу, коли ви готові приступити до комітів коду. Що б сталося, якби ми використовували командний рядок операційної системи для переміщення файлів замість команди git?</p>

<p>Виявляється, наступний набір команд ідентичний нашим останнім діям. Роботи тут побільше, але результат той самий.</p>

<p class="command"> Ми могли б виконати:</p>

<pre class="instructions">mkdir lib
mv hello.html lib
git add lib/hello.html
git rm hello.html</pre>

<h2><em>03</em> Коміт в новий каталог</h2>

<p>Давайте зробимо коміт цього переміщення.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git commit -m "Moved hello.html to lib"</pre>