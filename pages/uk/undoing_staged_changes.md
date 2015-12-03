---
view: page
title: "15. Скасування проіндексованих змін (перед комітом)"
---

<h3>Цілі</h3>

<ul><li>Навчитися скасовувати зміни, які було проіндексовано</li></ul>

<h2><em>01</em> Внесіть зміни у файл і проіндексуйте їх</h2>

<p>Внесіть зміни у файл <code>hello.html</code> у вигляді небажаного коментаря</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- This is an unwanted but staged comment --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Проіндексуйте ці зміни.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>02</em> Перевірте стан</h2>

<p>Перевірте стан небажаної зміни.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git status</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Стани показує, що зміни було проіндексовано і готове до коміту.</p>

<h2><em>03</em> Виконайте сброс буферної зони</h2>

<p>На щастя, вивід стану показує нам саме те, що ми повинні зробити для скасування індексації змін.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git reset HEAD hello.html</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git reset HEAD hello.html
Unstaged changes after reset:
M	hello.html</pre>

<p>Команда <code>reset</code> скидає буферну зону до <span class="caps">HEAD</span>. Це очищає буферну зону від змін, які ми щойно проіндексували.</p>

<p>Команда <code>reset</code> (за замовчуванням) не змінює робочий каталог. Тому робочий каталог все ще містить небажаний коментар. Ми можемо використовувати команду <code>checkout</code> з попереднього уроку, щоб видалити небажані зміни в робочому каталозі.</p>

<h2><em>04</em> Перейдіть на версію коміту</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout hello.html
git status</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>Наш робочий каталог знову чистий.</p>