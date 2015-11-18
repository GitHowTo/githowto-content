---
view: page
title: "3. Створення проекту"
---

<h3>Цілі</h3>

<ul><li>Навчитися створювати git репозиторій з нуля.</li></ul>

<h2><em>01</em> Створіть сторінку «Hello, World»</h2>

<p>Почніть роботу в порожньому робочему каталозі(наприклад Work, якщо ви завантажили архів з попереднього кроку) зі створення порожнього каталогу з ім'ям «hello», потім перейдіть до нього і створіть в ньому файл з ім'ям <code>hello.html</code> з наступним змістом.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">mkdir hello
cd hello
touch hello.html</pre>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file">Hello, World</pre>

<h2><em>02</em> Створіть репозиторій</h2>

<p>Зараз у вас є каталог з одним файлом. Щоб створити git репозиторій з цього каталогу, виконайте команду git init.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git init</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git init
Initialized empty Git repository in /Users/alex/Documents/Presentations/githowto/auto/hello/.git/
</pre>

<h2><em>03</em> Додайте сторінку у репозиторій</h2>

<p>Зараз давайте додамо в репозитарій сторінку «Hello, World».</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add hello.html
git commit -m "First Commit"</pre>

<p>Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git add hello.html
$ git commit -m "First Commit"
[master (root-commit) 911e8c9] First Commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 hello.html</pre>
