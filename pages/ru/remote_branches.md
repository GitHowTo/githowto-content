---
view: page
title: "40. Удаленные ветки"
---

<h3>Цели</h3>

<ul><li>Узнать о локальных и удаленных ветках</li></ul>

<p>Давайте посмотрим на ветки, доступные в нашем клонированном репозитории.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git branch</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git branch
* master</pre>

<p>Как мы видим, в списке только ветка master. Где ветка style? Команда <strong>git</strong> <strong>branch</strong> выводит только список локальных веток по умолчанию.</p>

<h2><em>01</em> Список удаленных веток</h2>

<p>Для того, чтобы увидеть все ветки, попробуйте следующую команду:</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git branch -a</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git branch -a
* master
  remotes/origin/HEAD -&gt; origin/master
  remotes/origin/style
  remotes/origin/master</pre>

<p>Git выводит все коммиты в оригинальный репозиторий, но ветки в удаленном репозитории не рассматриваются как локальные. Если мы хотим иметь собственную ветку <strong>style</strong>, мы должны сами ее создать. Через минуту вы увидите, как это делается.</p>