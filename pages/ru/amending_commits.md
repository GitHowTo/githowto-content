---
view: page
title: "19. Внесение изменений в коммиты"
---

<h3>Цели</h3>

<ul><li>Научиться изменять существующие коммиты</li></ul>

<h2><em>01</em> Измените страницу, а затем сделайте коммит</h2>

<p>Добавьте в страницу комментарий автора.</p>

<h4 class="h4-pre">Файл: <em style="text-transform: none">hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add hello.html
git commit -m "Add an author comment"</pre>

<h2><em>02</em> Ой... необходим email</h2>

<p>После совершения коммита вы понимаете, что любой хороший комментарий должен включать электронную почту автора. Обновите страницу hello, включив в нее email.</p>

<h4 class="h4-pre">Файл: <em  style="text-transform: none">hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Измените предыдущий коммит</h2>

<p>Мы действительно не хотим создавать отдельный коммит только ради электронной почты. Давайте изменим предыдущий коммит, включив в него адрес электронной почты.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add hello.html
git commit --amend -m "Add an author/email comment"</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git add hello.html
$ git commit --amend -m "Add an author/email comment"
[master 6a78635] Add an author/email comment
 1 files changed, 2 insertions(+), 1 deletions(-)</pre>

<h2><em>04</em> Просмотр истории</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist
* 6a78635 2011-03-09 | Add an author/email comment (HEAD, master) [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Мы можем увидеть, что оригинальный коммит «автор» заменен коммитом «автор/email». Этого же эффекта можно достичь путем сброса последнего коммита в ветке, и повторного коммита новых изменений.</p>
