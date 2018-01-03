---
view: page
title: "6. Індексація змін"
---

<h3>Цілі</h3>

<ul><li>Навчитися індексувати зміни для наступних комітів</li></ul>

<h2><em>01</em>Додайте зміни</h2>

<p>Зараз, дайте команду git проіндексувати зміни. Перевірте стан</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add hello.html
git status</pre>

<p>Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git add hello.html
$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Зміни файлу <code>hello.html</code> було проіндексовано. Це означає, що git тепер знає про зміни, але вони поки що <em>перманентно</em> (читай, <em>назавжди</em>) записані до репозиторію. Наступний коміт буде включати в себе проіндексовані зміни.</p>

<p>Якщо ви вирішили, що <em>не</em> хочете комітити зміни, команда стану нагадає вам про те, що за допомогою команди <code>git reset</code> можна зняти індексацію цих змін.</p>