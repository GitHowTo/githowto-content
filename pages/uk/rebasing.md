---
view: page
title: "34. Перебазування"
---

<h3>Цілі</h3>

<ul><li>Використовувати команду rebase замість команди merge.</li></ul>

<p>Отже, ми повернулися в точку до першого злиття і хочемо перенести зміни із master у нашу гілку style.</p>

<p>Цього разу для перенесення змін з гілки master ми будемо використовувати команду rebase замість merge.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout style
git rebase master
git hist</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ go style
Switched to branch 'style'
$
$ git rebase master
First, rewinding head to replay your work on top of it...
Applying: Added css stylesheet
Applying: Hello uses style.css
Applying: Updated index.html
$
$ git hist
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, style) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README (master) [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<h2><em>01</em> Злиття VS перебазування</h2>

<p>Кінцевий результат перебазування дуже схожий на результат злиття. Гілка style в даний час містить всі свої зміни, а також всі зміни гілки master. Однак, дерево комітів значно відрізняється. Дерево комітів гілки style було переписано таким чином, що гілка master є частиною історії комітів. Це робить ланцюг комітів лінійним і набагато більш читабельним.</p>

<h2><em>02</em> Коли використовувати перебазування, а коли злиття?</h2>

<p>Не використовуйте перебазування …</p>

<ol>
<li>Якщо гілка є публічною і розшаренною. Переписування загальних гілок заважатиме роботі інших членів команди.</li>
<li>Коли важлива <em>точна</em> історія комітів гілки (тому що команда rebase переписує історію комітів).</li>
</ol>
<p>Враховуючи наведені вище рекомендації, я волію використовувати rebase для короткочасних, локальних гілок, а злиття для гілок у публічному репозиторію.</p>