---
view: page
title: "37. Клонирование репозиториев"
---

<h3>Цели</h3>

<ul><li>Научиться делать копии репозиториев.</li></ul>

<p>Если вы работаете в команде, последующие 12 глав довольно важны в понимании, т.к. вы почти всегда будете работать с клонированными репозиториями.</p>

<h2><em>01</em> Перейдите в рабочий каталог</h2>

<p>Перейдите в рабочий каталог и сделайте клон вашего репозитория hello.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">cd ..
pwd
ls</pre>

<p style="color:red;"><strong><span class="caps">Примечание</span>: Сейчас мы находимся  в рабочем каталоге.</strong></p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cd ..
$ pwd
/Users/alex/Documents/Presentations/githowto/auto
$ ls
hello</pre>

<p>В этот момент вы должны находиться в «рабочем» каталоге. Здесь должен быть единственный репозиторий под названием «hello».</p>

<h2><em>02</em> Создайте клон репозитория hello</h2>

<p>Давайте создадим клон репозитория.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git clone hello cloned_hello
ls</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git clone hello cloned_hello
Cloning into cloned_hello...
done.
$ ls
cloned_hello
hello</pre>

<p>В вашем рабочем каталоге теперь должно быть два репозитория: оригинальный репозиторий «hello» и клонированный репозиторий «cloned_hello»</p>