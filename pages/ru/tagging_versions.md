---
view: page
title: "13. Создание тегов версий"
---

<h3>Цели</h3>

<ul><li>Узнать, как создавать теги для коммитов для использования в будущем</li></ul>

<p>Давайте назовем текущую версию страницы hello первой (<em>v1</em>).</p>

<h2><em>01</em> Создайте тег первой версии</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git tag v1</pre>

<p>Теперь текущая версия страницы называется <em>v1</em>.</p>

<h2><em>02</em> Теги для предыдущих версий </h2>

<p>Давайте создадим тег для версии, которая идет перед текущей версией и назовем его <em>v1-beta</em>. В первую очередь нам надо переключиться на предыдущую версию. Вместо поиска по хэшу, мы будем использовать <code>^</code>, обозначающее «родитель v1».</p>

<p class="note">Если обозначение <code>v1^</code> вызывает у вас какие-то проблемы, попробуйте также <code>v1~1</code>, указывающее на ту же версию.  Это обозначение можно определить как «первую версию предшествующую v1».</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout v1^
cat hello.html</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout v1^
Note: checking out 'v1^'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 8c32287... Added standard HTML page tags
$ cat hello.html
&lt;html&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Это версия c тегами <code>&lt;html&gt;</code> и <code>&lt;body&gt;</code>, но еще <em>пока</em> без  <code>&lt;head&gt;</code>. Давайте сделаем ее версией <em>v1-beta</em>.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git tag v1-beta</pre>

<h2><em>03</em> Переключение по имени тега </h2>

<p>Теперь попробуйте попереключаться между двумя отмеченными версиями.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout v1
git checkout v1-beta</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout v1
Previous HEAD position was 8c32287... Added standard HTML page tags
HEAD is now at fa3c141... Added HTML header
$ git checkout v1-beta
Previous HEAD position was fa3c141... Added HTML header
HEAD is now at 8c32287... Added standard HTML page tags</pre>

<h2><em>04</em> Просмотр тегов с помощью команды <code>tag</code></h2>

<p>Вы можете увидеть, какие теги доступны, используя команду <code>git tag</code>.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git tag</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git tag
v1
v1-beta</pre>

<h2><em>05</em> Просмотр Тегов в логах </h2>

<p>Вы также можете посмотреть теги в логе.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist master --all</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist master --all
* fa3c141 2011-03-09 | Added HTML header (v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (HEAD, v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Вы можете видеть теги (<code>v1</code> и <code>v1-beta</code>) в логе вместе с именем ветки (<code>master</code>). Кроме того <code>HEAD</code> показывает коммит, на который вы переключились (на данный момент это <code>v1-beta</code>).</p>