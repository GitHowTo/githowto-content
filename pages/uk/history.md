---
view: page
title: "10. Історія"
---

<h3>Цілі</h3>

<ul><li>Навчитися продивлятися історію проекту.</li></ul>

<p>Отримання списку зроблених змін — функція команди <code>git log</code>.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git log</pre>

<p>Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git log
commit fa3c1411aa09441695a9e645d4371e8d749da1dc
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added HTML header

commit 8c3228730ed03116815a5cc682e8105e7d981928
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added standard HTML page tags

commit 43628f779cb333dd30d78186499f93638107f70b
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added h1 tag

commit 911e8c91caeab8d30ad16d56746cbd6eef72dc4c
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    First Commit</pre>

<p>Ось список усіх чотирьох комітів у репозиторій, котрі ми встигли створити.</p>

<h2><em>01</em> Однорядкова історія</h2>

<p>Ви повністю контролюєте те, що відображає <code>log</code>. Мені, наприклад, подобається однорядковий формат:</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git log --pretty=oneline</pre>

<p>Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git log --pretty=oneline
fa3c1411aa09441695a9e645d4371e8d749da1dc Added HTML header
8c3228730ed03116815a5cc682e8105e7d981928 Added standard HTML page tags
43628f779cb333dd30d78186499f93638107f70b Added h1 tag
911e8c91caeab8d30ad16d56746cbd6eef72dc4c First Commit</pre>

<h2><em>02</em> Контроль відображення записів</h2>

<p>Існує багато варіантів вибору, які елементи відображати у лозі. Пограйтесь з наступними параметрами:</p>

<pre class="instructions">git log --pretty=oneline --max-count=2
git log --pretty=oneline --since='5 minutes ago'
git log --pretty=oneline --until='5 minutes ago'
git log --pretty=oneline --author=&lt;your name&gt;
git log --pretty=oneline --all</pre>

<p>Подробиці в інструкції <code>git-log</code>.</p>

<h2><em>03</em> Ухитряємося</h2>

<p>Ось що я використовую для перегляду змін, зроблених за останній тиждень. Я додаю <code>--author=alex</code>, якщо я хочу бачити лише зміни, зроблені мною.</p>

<pre class="instructions">git log --all --pretty=format:"%h %cd %s (%an)" --since='7 days ago'</pre>

<h2><em>04</em> Кінцевый формат логу</h2>

<p>З часом, я вирішив, що для більшій частини моєї роботи мені підходить наступий формат логу.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short</pre>

<p>Виглядає це десь так:</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Давайте роздивимось його детальніше:</p>

<ul>
<li><code>--pretty="..."</code> — визначає формат виходу.</li>
<li><code>%h</code> — скрочений хеш коміту</li>
<li><code>%d</code> — доповнення коміту(«голови» гілок ии теги)</li>
<li><code>%ad</code> — дата коміту</li>
<li><code>%s</code> — коментар</li>
<li><code>%an</code> — им'я автора</li>
<li><code>--graph</code> — відображає дерево комітів у видгляді <span class="caps">ASCII</span>-графіку</li>
<li><code>--date=short</code> — зберігає формат дати коротким й симпатичним</li>
</ul>

<p>Таким чином, кожного разу, коли ви захочите подивитись лог, вам прийдеться багато друкувати. На щастя, ми дізнаємось про git алиаси в наступному уроці.</p>

<h2><em>05</em> Інші інструменти</h2>

<p><code>gitx</code> (для Mac) й <code>gitk</code> (для інших платформ) корисні у вивчені історії змін.</p>
