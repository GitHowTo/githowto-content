---
view: page
title: "9. Изменения, а не файлы"
---

<h3>Цели</h3>

<ul><li>Понять, что git работает с изменениями, а не файлами.</li></ul>

<p>Большинство систем версионного контроля работают с файлами. Вы добавляете файл в версионный контроль, а система отслеживает изменения файла с этого момента.</p>

<p>Git фокусируется на изменениях в файле, а не самом файле. Когда вы осуществляете команду <code>git add file</code>,  вы не говорите git добавить файл в репозиторий. Скорее вы говорите, что git надо отметить текущее состояние файла, коммит которого будет произведен позже.</p>

<p>Мы попытаемся исследовать эту разницу в данном уроке.</p>

<h2><em>01</em> Первое изменение: Добавьте стандартные теги страницы</h2>

<p>Измените страницу «Hello, World», чтобы она содержала стандартные теги <code>&lt;html&gt;</code> и <code>&lt;body&gt;</code>.</p>

<h4 class="h4-pre">Файл: <em style="text-transform: none">hello.html</em></h4>

<pre class="file"><strong>&lt;html&gt;
  &lt;body&gt;</strong>
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  <strong>&lt;/body&gt;
&lt;/html&gt;</strong></pre>

<h2><em>02</em> Добавьте это изменение</h2>

<p>Теперь добавьте это изменение в индекс git.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>03</em> Второе изменение: Добавьте заголовки HTML</h2>

<p>Теперь добавьте заголовки HTML (секцию <code>&lt;head&gt;</code>) к странице «Hello, World».</p>

<h4 class="h4-pre">Файл: <em style="text-transform: none">hello.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>04</em> Проверьте текущий статус</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git status</pre>

<p>Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#</pre>

<p>Обратите внимание на то, что <code>hello.html</code> указан дважды в состоянии. Первое изменение (добавление стандартных тегов) проиндексировано и готово к коммиту. Второе изменение (добавление заголовков HTML) является непроиндексированным. Если бы вы делали коммит сейчас, заголовки не были бы сохранены в репозиторий.</p>

<p>Давайте проверим.</p>

<h2><em>05</em> Коммит</h2>

<p>Произведите коммит проиндексированного изменения (значение по умолчанию), а затем еще раз проверьте состояние.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git commit -m "Added standard HTML page tags"
git status</pre>

<p>Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git commit -m "Added standard HTML page tags"
[master 8c32287] Added standard HTML page tags
 1 files changed, 3 insertions(+), 1 deletions(-)
$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>Состояние команды говорит о том, что <code>hello.html</code> имеет незафиксированные изменения, но уже не в буферной зоне.</p>

<h2><em>06</em> Добавьте второе изменение</h2>

<p>Теперь добавьте второе изменение в индекс, а затем проверьте состояние с помощью команды <code>git status</code>.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add .
git status</pre>

<p class="note"><strong>Примечание:</strong> В качестве файла для добавления, мы использовали текущий каталог («.»). Это самый краткий и удобный способ добавления всех изменений в файлы текущего каталога и его подкаталоги. Но поскольку он добавляет все, <em>не лишним</em> будет проверить состояние перед запуском <code>add</code>, просто чтобы убедиться, что вы не добавили какой-то файл, который добавлять было не нужно.</p>

<p class="note">Я хотел показать вам трюк с <code>add</code>, далее мы будем на всякий случай продолжать добавлять явные файлы.</p>

<p>Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Второе изменение было проиндексировано и готово к коммиту.</p>

<h2><em>07</em> Сделайте коммит второго изменения</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git commit -m "Added HTML header"</pre>
