---
view: page
title: "39. Что такое origin?"
---

<h3>Цели</h3>

<ul><li>Узнать об именах удаленных репозиториев.</li></ul>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git remote</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git remote
origin</pre>

<p>Мы видим, что клонированный репозиторий знает об имени по умолчанию удаленного репозитория. Давайте посмотрим, можем ли мы получить более подробную информацию об имени по умолчанию:</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git remote show origin</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git remote show origin
* remote origin
  Fetch URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  Push  URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  HEAD branch (remote HEAD is ambiguous, may be one of the following):
    style
    master
  Remote branches:
    style  tracked
    master tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)</pre>

<p>Мы видим, что «имя по умолчанию» удаленного репозитория – оригинальное <strong>hello</strong>. Удаленные репозитории обычно размещаются на отдельной машине, возможно, централизованном сервере. Однако, как мы видим здесь,  они могут с тем же успехом указывать на репозиторий на той же машине. Нет ничего особенного в «имени по умолчанию», однако существует традиция  использовать «имя по умолчанию» на первичном централизованном репозитории (если таковой имеется).</p>