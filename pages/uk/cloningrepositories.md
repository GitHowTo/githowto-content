---
view: page
title: "37. Клонування репозиторіїв"
---

<h3>Цілі</h3>

<ul><li>Навчитися робити копії репозиторіїв.</li></ul>

<p>Якщо ви працюєте в команді, наступні 12 розділів досить важливі в розумінні, тому що ви майже завжди будете працювати з клонованими репозиторіями.</p>

<h2><em>01</em> Перейдіть в робочий каталог</h2>

<p>Перейдіть в робочий каталог і зробіть клон вашого сховища hello.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cd ..
pwd
ls</pre>

<p style="color:red;"><strong><span class="caps">Примітка</span>: Зараз ми знаходимося в робочому каталозі.</strong></p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cd ..
$ pwd
/Users/alex/Documents/Presentations/githowto/auto
$ ls
hello</pre>

<p>У цей момент ви повинні знаходитися в «робочому» каталозі. Тут має бути єдиний репозиторій під назвою «hello».</p>

<h2><em>02</em> Створіть клон репозиторію hello</h2>

<p>Давайте створимо клон репозиторію.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git clone hello cloned_hello
ls</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git clone hello cloned_hello
Cloning into cloned_hello...
done.
$ ls
cloned_hello
hello</pre>

<p>У вашому робочому каталозі тепер має бути два репозиторія: оригінальний репозиторій «hello» і клонований репозиторій «cloned_hello»</p>