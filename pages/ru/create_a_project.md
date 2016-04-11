---
view: page
title: "3. Создание проекта"
---

<h3>Цели</h3>

<ul><li>Научиться создавать git репозиторий с нуля.</li></ul>

<h2><em>01</em> Создайте страницу «Hello, World»</h2>

<p>Начните работу в пустом рабочем каталоге (например Work, если вы скачали архив с предыдущего шага) с создания пустого каталога с именем «hello», затем войдите внего и создайте там файл с именем <code>hello.html</code> с таким содержанием.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">mkdir hello
cd hello
touch hello.html</pre>

<h4 class="h4-pre">Файл: <em style="text-transform: none">hello.html</em></h4>

<pre class="file">Hello, World</pre>

<h2><em>02</em> Создайте репозиторий</h2>

<p>Теперь у вас есть каталог с одним файлом. Чтобы создать git репозиторий из этого каталога, выполните команду git init.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git init</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git init
Initialized empty Git repository in /Users/alex/Documents/Presentations/githowto/auto/hello/.git/
</pre>

<h2><em>03</em> Добавьте страницу в репозиторий</h2>

<p>Теперь давайте добавим в репозиторий страницу «Hello, World».</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add hello.html
git commit -m "First Commit"</pre>

<p>Вы увидите …</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git add hello.html
$ git commit -m "First Commit"
[master (root-commit) 911e8c9] First Commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 hello.html</pre>
