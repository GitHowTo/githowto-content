---
view: page
title: "43. Слияние извлеченных изменений"
---

<h3>Цели</h3>

<ul><li>Научиться перемещать извлеченные изменения в текущую ветку и рабочий каталог.</li></ul>

<h2><em>01</em> Слейте извлеченные изменения в локальную ветку master</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git merge origin/master</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git merge origin/master
Updating 6e6c76a..2faa4ea
Fast-forward
 README |    1 +
 1 files changed, 1 insertions(+), 0 deletions(-)</pre>

<h2><em>02</em> Еще раз проверьте файл <span class="caps">README</span></h2>

<p>Сейчас мы должны увидеть изменения.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">cat README</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.
(changed in original)</pre>

<p>Вот и изменения. Хотя команда «git fetch» не сливает изменения, мы можем вручную слить изменения из удаленного репозитория.</p>

<h2><em>03</em> Далее</h2>

<p>Теперь давайте рассмотрим объединение fetch &amp; merge в одну команду.</p>