---
view: page
title: "10. История"
---

<h3>Цели</h3>

<ul><li>Научиться просматривать историю проекта.</li></ul>

<p>Получение списка произведенных изменений — функция команды <code>git log</code>.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git log</pre>

<p>Вы увидите…</p>

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

<p>Вот список всех четырех коммитов в репозиторий, которые мы успели совершить.</p>

<h2><em>01</em> Однострочная история</h2>

<p>Вы полностью контролируете то, что отображает <code>log</code>. Мне, например, нравится однострочный формат:</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git log --pretty=oneline</pre>

<p>Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git log --pretty=oneline
fa3c1411aa09441695a9e645d4371e8d749da1dc Added HTML header
8c3228730ed03116815a5cc682e8105e7d981928 Added standard HTML page tags
43628f779cb333dd30d78186499f93638107f70b Added h1 tag
911e8c91caeab8d30ad16d56746cbd6eef72dc4c First Commit</pre>

<h2><em>02</em> Контроль отображения записей</h2>

<p>Есть много вариантов выбора, какие элементы отображаются в логе. Поиграйте со следующими параметрами:</p>

<pre class="instructions">git log --pretty=oneline --max-count=2
git log --pretty=oneline --since='5 minutes ago'
git log --pretty=oneline --until='5 minutes ago'
git log --pretty=oneline --author=&lt;your name&gt;
git log --pretty=oneline --all</pre>

<p>Подробности в инструкции <code>git-log</code>.</p>

<h2><em>03</em> Изощряемся</h2>

<p>Вот что я использую для просмотра изменений, сделанных за последнюю неделю. Я добавлю <code>--author=alex</code>, если я хочу увидеть только изменения, которые сделала я.</p>

<pre class="instructions">git log --all --pretty=format:"%h %cd %s (%an)" --since='7 days ago'</pre>

<h2><em>04</em> Конечный формат лога</h2>

<p>Со временем, я решила, что для большей части моей работы мне подходит следующий формат лога.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short</pre>

<p>Выглядит это примерно так:</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Давайте рассмотрим его в деталях:</p>

<ul>
<li><code>--pretty="..."</code> — определяет формат вывода.</li>
<li><code>%h</code> — укороченный хэш коммита</li>
<li><code>%d</code> — дополнения коммита («головы» веток или теги)</li>
<li><code>%ad</code> — дата коммита</li>
<li><code>%s</code> — комментарий</li>
<li><code>%an</code> — имя автора</li>
<li><code>--graph</code> — отображает дерево коммитов в виде <span class="caps">ASCII</span>-графика</li>
<li><code>--date=short</code> — сохраняет формат даты коротким и симпатичным</li>
</ul>

<p>Таким образом, каждый раз, когда вы захотите посмотреть лог, вам придется много печатать. К счастью, мы узнаем о git алиасах в следующем уроке.</p>

<h2><em>05</em> Другие инструменты</h2>

<p>Оба <code>gitx</code> (для Mac) и <code>gitk</code> (для любой платформы) полезны в изучении истории изменений.</p>