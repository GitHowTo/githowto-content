---
view: page
title: "22. Git всередині: Каталог .git"
---

<h3>Ціл</h3>

<ul><li>Дізнатися про структуру каталогу <code>.git</code></li></ul>

<h2><em>01</em> Каталог <code>.git</code></h2>

<p>Настав час провести невелике дослідження. Для початку, з кореневого каталогу вашого проекту…</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">ls -C .git</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ ls -C .git
COMMIT_EDITMSG	MERGE_RR	config		hooks		info		objects		rr-cache
HEAD		ORIG_HEAD	description	index		logs		refs</pre>

<p>Це магічний каталог, в якому зберігаються всі «матеріали» git. Давайте заглянемо в каталог об'єктів.</p>

<h2><em>02</em> База даних об'єктів</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">ls -C .git/objects</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ ls -C .git/objects
09	24	28	45	59	6a	77	80	8c	97	af	c4	e7	info
11	27	43	56	69	6b	78	84	91	9c	b5	e4	fa	pack</pre>

<p>Ви повинні побачити купу каталогів, імена яких складаються з 2 символів. Імена каталогів є першими двома буквами хеша sha1 об'єкта, що зберігається в git.</p>

<h2><em>03</em> Заглиблюємося в базу даних об'єктів</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">ls -C .git/objects/&lt;dir&gt;</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ ls -C .git/objects/09
6b74c56bfc6b40e754fc0725b8c70b2038b91e	9fb6f9d3a104feb32fcac22354c4d0e8a182c1</pre>

<p>Дивимося в один з каталогів з ім'ям з 2 букв. Ви побачите файли з іменами з 38 символів. Це файли, що містять об'єкти, що зберігаються в git. Вони стиснуті і закодовані, тому перегляд їх вмісту нам мало чим допоможе.
Розглянемо далі каталог .git уважно</p>

<h2><em>04</em> Config File</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cat .git/config</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cat .git/config
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
	ignorecase = true
[user]
	name = Alexander Shvets
	email = alex@githowto.com</pre>

<p>Це файл конфігурації, що створюється для кожного конкретного проекту. Записи в цьому файлі будуть перезаписувати записи у файлі <code>.gitconfig</code> вашого головного каталогу, принаймні в рамках цього проекту.</p>

<h2><em>05</em> Гілки і теги</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">ls .git/refs
ls .git/refs/heads
ls .git/refs/tags
cat .git/refs/tags/v1</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ ls .git/refs
heads
tags
$ ls .git/refs/heads
master
$ ls .git/refs/tags
v1
v1-beta
$ cat .git/refs/tags/v1
fa3c1411aa09441695a9e645d4371e8d749da1dc</pre>

<p>Ви повинні впізнавати файли в підкаталозі тегів. Кожен файл відповідає тегу, раніше створеному за допомогою команди <code>git tag</code>. Його зміст - це всього лише хеш комітов, прив'язаний до тегу.</p>

<p>Каталог <em>heads</em> практично аналогічний, але використовується для гілок, а не тегів. На даний момент у нас є тільки одна гілка, тому все, що ви побачите в цьому каталозі - це гілка <em>master</em>.</p>

<h2><em>06</em> Файл <span class="caps">HEAD</span></h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cat .git/HEAD</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cat .git/HEAD
ref: refs/heads/master</pre>

<p>Файл <span class="caps">HEAD</span> містить посилання на поточну гілку, в даний момент це повинна бути гілка master.</p>