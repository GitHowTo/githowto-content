---
view: page
title: "43. Злиття витягнутих змін"
---

<h3>Цілі</h3>

<ul><li>Навчитися переміщувати витягнуті зміни в поточну гілку і робочий каталог.</li></ul>

<h2><em>01</em> Злийте витягнуті зміни в локальну гілку master</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git merge origin/master</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git merge origin/master
Updating 6e6c76a..2faa4ea
Fast-forward
 README |    1 +
 1 files changed, 1 insertions(+), 0 deletions(-)</pre>

<h2><em>02</em> Ще раз перевірте файл <span class="caps">README</span></h2>

<p>Зараз ми повинні побачити зміни.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cat README</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.
(changed in original)</pre>

<p>Ось і зміни. Хоча команда «git fetch» не зливає зміни, ми можемо вручну злити зміни з віддаленого репозиторію.</p>

<h2><em>03</em> Далі</h2>

<p>Тепер давайте розглянемо об'єднання fetch &amp; merge в одну команду.</p>