---
view: page
title: "14. Скасування локальних змін (до індексації)"
---

<h3>Цілі</h3>

<ul><li>Навчитися скасовувати зміни в робочому каталозі</li></ul>

<h2><em>01</em> Перейдіть на гілку Master </h2>

<p>Переконайтеся, що ви перебуваєте на останньому коміті гілки master, перш ніж продовжити роботу.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout master</pre>

<h2><em>02</em> Змініть hello.html </h2>

<p>Іноді трапляється, що ви змінили файл в робочому каталозі, і хочете скасувати останні коміти. З цим впорається команда <code>checkout</code>.</p>

<p>Внесіть зміни у файл hello.html у вигляді небажаного коментаря.</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is a bad comment.  We want to revert it. --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Перевірте стан </h2>

<p>Спочатку перевірте стан робочого каталогу.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git status</pre>

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

<p>Ми бачимо, що файл <code>hello.html</code> було змінено, але ще не проіндексовано.</p>

<h2><em>04</em> Скасування змін в робочому каталозі </h2>

<p>Використовуйте команду <code>checkout</code> для перемикання в версію файлу <code>hello.html</code> у репозиторію.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout hello.html
git status
cat hello.html</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout hello.html
$ git status
# On branch master
nothing to commit (working directory clean)
$ cat hello.html
&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Команда <code>status</code> показує нам, що не було зроблено ніяких змін не зафіксованих в робочому каталозі. І «небажаний коментар» більше не є частиною вмісту файлу.</p>