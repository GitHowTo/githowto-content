---
view: page
title: "14. Отмена локальных изменений (до индексации)"
---

<h3>Цели</h3>

<ul><li>Научиться отменять изменения в рабочем каталоге</li></ul>

<h2><em>01</em> Переключитесь на ветку Master </h2>

<p>Убедитесь, что вы находитесь на последнем коммите ветки master, прежде чем продолжить работу.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout master</pre>

<h2><em>02</em> Измените hello.html </h2>

<p>Иногда случается, что вы изменили файл в рабочем каталоге, и хотите отменить последние коммиты. С этим справится команда <code>checkout</code>.</p>

<p>Внесите изменение в файл hello.html в виде нежелательного комментария.</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is a bad comment.  We want to revert it. --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Проверьте состояние </h2>

<p>Сначала проверьте состояние рабочего каталога.</p>

<h4 class="h4-pre">Выполните:</h4>

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

<p>Мы видим, что файл <code>hello.html</code> был изменен, но еще не проиндексирован.</p>

<h2><em>04</em> Отмена изменений в рабочем каталоге </h2>

<p>Используйте команду <code>checkout</code> для переключения в версию файла <code>hello.html</code> в репозитории.</p>

<h4 class="h4-pre">Выполните:</h4>

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

<p>Команда <code>status</code> показывает нам, что не было произведено никаких изменений, не зафиксированных в рабочем каталоге. И «нежелательный комментарий» больше не является частью содержимого файла.</p>