---
view: page
title: "45. Добавление ветки наблюдения"
---

<h3>Цели</h3>

<ul><li>Научиться добавлять локальную ветку, которая отслеживает изменения удаленной ветки.</li></ul>

<p>Ветки, которые начинаются с remotes/origin являются ветками оригинального репозитория. Обратите внимание, что у вас больше нет ветки под названием style, но он знает, что в оригинальном репозитории ветка style была.</p>

<h2><em>01</em> Добавьте локальную ветку, которая отслеживает удаленную ветку.</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git branch --track style origin/style
git branch -a
git hist --max-count=2</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git branch --track style origin/style
Branch style set up to track remote branch style from origin.
$ git branch -a
  style
* master
  remotes/origin/HEAD -&gt; origin/master
  remotes/origin/style
  remotes/origin/master
$ git hist --max-count=2
* 2faa4ea 2011-03-09 | Changed README in original repo (HEAD, origin/master, origin/HEAD, master) [Alexander Shvets]
* 6e6c76a 2011-03-09 | Updated index.html (origin/style, style) [Alexander Shvets]</pre>

<p>Теперь мы можем видеть ветку style в списке веток и логе.</p>