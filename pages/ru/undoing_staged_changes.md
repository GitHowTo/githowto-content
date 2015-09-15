---
view: page
title: "15. Отмена проиндексированных изменений (перед коммитом)"
---

<h3>Цели</h3>

<ul><li>Научиться отменять изменения, которые были проиндексированы</li></ul>

<h2><em>01</em> Измените файл и проиндексируйте изменения</h2>

<p>Внесите изменение в файл <code>hello.html</code> в виде нежелательного комментария</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- This is an unwanted but staged comment --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Проиндексируйте это изменение.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>02</em> Проверьте состояние</h2>

<p>Проверьте состояние нежелательного изменения.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git status</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Состояния показывает, что изменение было проиндексировано и готово к коммиту.</p>

<h2><em>03</em> Выполните сброс буферной зоны</h2>

<p>К счастью, вывод состояние показывает нам именно то, что мы должны сделать для отмены индексации изменения.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git reset HEAD hello.html</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git reset HEAD hello.html
Unstaged changes after reset:
M	hello.html</pre>

<p>Команда <code>reset</code> сбрасывает буферную зону к <span class="caps">HEAD</span>. Это очищает буферную зону от изменений, которые мы только что проиндексировали.</p>

<p>Команда <code>reset</code> (по умолчанию) не изменяет рабочий каталог. Поэтому рабочий каталог все еще содержит нежелательный комментарий. Мы можем использовать команду <code>checkout</code> из предыдущего урока, чтобы удалить нежелательные изменения в рабочем каталоге.</p>

<h2><em>04</em> Переключитесь на версию коммита</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout hello.html
git status</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>Наш рабочий каталог опять чист.</p>