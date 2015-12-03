---
view: page
title: "26. Зміни в гілці master"
---

<h3>Цілі</h3>

<ul><li>Навчитися працювати з декількома гілками з різними (і, можливо, конфліктуючими) змінами.</li></ul>

<p>Поки ви міняли гілку «style», хтось вирішив оновити гілку master. Вони додали <span class="caps">README</span>.</p>

<h2><em>01</em> Оновіть файл <span class="caps">README</span> зі змінами.</h2>

<h4 class="h4-pre">Файл: <em><span class="caps">README</span></em></h4>

<pre class="file">This is the Hello World example from the git tutorial.</pre>

<h2><em>02</em> Зробіть коміт змін <span class="caps">README</span> у гілку master.</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added README"</pre>