---
view: page
title: "45. Додавання гілки відстеження"
---

<h3>Цілі</h3>

<ul><li>Навчитися додавати локальну гілку, котра відслідковує зміни віддаленої гілки.</li></ul>

<p>Гілки, котрі починаються з remotes/origin є гілками оригінального репозиторію. Зверніть увагу, що у вас більш немає гілки з назвою style, але він знає, що в оригінальному репозиторію гілка style була.</p>

<h2><em>01</em> Додайте локальну гілку, котра відслідковує віддалену гілку.</h2>

<h4 class="h4-pre">Виконайте:</h4>

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

<p>Тепер ми можемо бачити гілку style у списку гілок і у лозі.</p>
