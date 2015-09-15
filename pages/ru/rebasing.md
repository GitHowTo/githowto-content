---
view: page
title: "34. Перебазирование"
---

<h3>Цели</h3>

<ul><li>Использовать команду rebase вместо команды merge.</li></ul>

<p>Итак, мы вернулись в точку до первого слияния и хотим перенести изменения в master в нашу ветку style.</p>

<p>На этот раз для переноса изменений из ветки master мы будем использовать команду rebase вместо слияния.</p>

<h4 class="h4-pre">Выполните:</h4>

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

<h2><em>01</em> Слияние VS перебазирование</h2>

<p>Конечный результат перебазирования очень похож на результат слияния. Ветка style в настоящее время содержит все свои изменения, а также все изменения ветки master. Однако, дерево коммитов значительно отличается. Дерево коммитов ветки style было переписано таким образом, что ветка master является частью истории коммитов. Это делает цепь коммитов линейной и гораздо более читабельной.</p>

<h2><em>02</em> Когда использовать перебазирование, а когда слияние?</h2>

<p>Не используйте перебазирование …</p>

<ol>
<li>Если ветка является публичной и расшаренной. Переписывание общих веток будет мешать работе других членов команды.</li>
<li>Когда важна <em>точная</em> история коммитов ветки (так как команда rebase переписывает историю коммитов).</li>
</ol>
<p>Учитывая приведенные выше рекомендации, я предпочитаю использовать rebase для кратковременных, локальных веток, а слияние для веток в публичном репозитории.</p>