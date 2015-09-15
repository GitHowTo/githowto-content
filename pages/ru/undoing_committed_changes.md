---
view: page
title: "16. Отмена коммитов"
---

<h3>Цели</h3>

<ul><li>Научиться отменять коммиты в локальный репозиторий.</li></ul>

<h2><em>01</em> Отмена коммитов</h2>

<p>Иногда вы понимаете, что новые коммиты являются неверными, и хотите их отменить. Есть несколько способов решения этого вопроса, здесь мы будем использовать самый безопасный.</p>

<p>Мы отменим коммит путем создания нового коммита, отменяющего нежелательные изменения.</p>

<h2><em>02</em> Измените файл и сделайте коммит</h2>

<p>Измените файл <code>hello.html</code> на следующий.</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is an unwanted but committed change --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add hello.html
git commit -m "Oops, we didn't want this commit"</pre>

<h2><em>03</em> Сделайте коммит с новыми изменениями, отменяющими предыдущие</h2>

<p>Чтобы отменить коммит, нам необходимо сделать коммит, который удаляет изменения, сохраненные нежелательным коммитом.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git revert HEAD</pre>

<p>Перейдите в редактор, где вы можете отредактировать коммит-сообщение по умолчанию или оставить все как есть. Сохраните и закройте файл. Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git revert HEAD --no-edit
[master 45fa96b] Revert "Oops, we didn't want this commit"
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>Так как мы отменили самый последний произведенный коммит, мы смогли использовать <code>HEAD</code> в качестве аргумента для отмены. Мы можем отменить любой произвольной коммит в истории, указав его хэш-значение.</p>

<p class="note"><strong>Примечание:</strong> Команду <code>--no-edit</code> можно проигнорировать. Она была необходима для генерации выходных данных без открытия редактора.</p>

<h2><em>04</em> Проверьте лог</h2>

<p>Проверка лога показывает нежелательные и отмененные коммиты в наш репозиторий.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (HEAD, master) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Эта техника будет работать с любым коммитом (хотя, возможно, возникнут конфликты). Она безопасна в использовании даже в публичных ветках удаленных репозиториев.</p>

<h2><em>05</em> Далее</h2>

<p>Далее давайте посмотрим на технику, которая может быть использована для удаления последних коммитов из истории репозитория.</p>