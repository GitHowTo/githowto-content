---
view: page
title: "22. Git внутри: Каталог .git"
---

<h3>Цели</h3>

<ul><li>Узнать о структуре каталога <code>.git</code></li></ul>

<h2><em>01</em> Каталог <code>.git</code></h2>

<p>Настало время провести небольшое исследование. Для начала, из корневого каталога вашего проекта…</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">ls -C .git</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ ls -C .git
COMMIT_EDITMSG	MERGE_RR	config		hooks		info		objects		rr-cache
HEAD		ORIG_HEAD	description	index		logs		refs</pre>

<p>Это магический каталог, в котором хранятся все «материалы» git. Давайте заглянем в каталог объектов.</p>

<h2><em>02</em> База данных объектов</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">ls -C .git/objects</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ ls -C .git/objects
09	24	28	45	59	6a	77	80	8c	97	af	c4	e7	info
11	27	43	56	69	6b	78	84	91	9c	b5	e4	fa	pack</pre>

<p>Вы должны увидеть кучу каталогов, имена которых состоят из 2 символов. Имена каталогов являются первыми двумя буквами хэша sha1 объекта, хранящегося в git.</p>

<h2><em>03</em> Углубляемся в базу данных объектов</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">ls -C .git/objects/&lt;dir&gt;</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ ls -C .git/objects/09
6b74c56bfc6b40e754fc0725b8c70b2038b91e	9fb6f9d3a104feb32fcac22354c4d0e8a182c1</pre>

<p>Смотрим в один из каталогов с именем из 2 букв. Вы увидите файлы с именами из 38 символов. Это файлы, содержащие объекты, хранящиеся в git. Они сжаты и закодированы, поэтому просмотр их содержимого нам мало чем поможет.
Рассмотрим  далее каталог .git внимательно</p>

<h2><em>04</em> Config File</h2>

<h4 class="h4-pre">Выполните:</h4>

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

<p>Это файл конфигурации, создающийся для каждого конкретного проекта. Записи в этом файле будут перезаписывать записи в файле <code>.gitconfig</code> вашего главного каталога, по крайней мере в рамках этого проекта.</p>

<h2><em>05</em> Ветки и теги</h2>

<h4 class="h4-pre">Выполните:</h4>

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

<p>Вы должны узнавать файлы в подкаталоге тегов. Каждый файл соответствует тегу, ранее созданному с помощью команды <code>git tag</code>. Его содержание – это всего лишь хэш коммита, привязанный к тегу.</p>

<p>Каталог <em>heads</em> практически аналогичен, но используется для веток, а не тегов. На данный момент у нас есть только одна ветка, так что все, что вы увидите в этом каталоге – это ветка <em>master</em>.</p>

<h2><em>06</em> Файл <span class="caps">HEAD</span></h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">cat .git/HEAD</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cat .git/HEAD
ref: refs/heads/master</pre>

<p>Файл <span class="caps">HEAD</span> содержит ссылку на текущую ветку, в данный момент это должна быть ветка master.</p>