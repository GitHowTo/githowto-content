---
view: page
title: "44. Извлечение и слияние изменений"
---

<h3>Цели</h3>

<ul><li>Узнать о том, что команда <code>git pull</code> эквивалентна комбинации <code>git fetch</code> и <code>git merge</code>.</li></ul>

<h3> Обсуждение </h3>

<p>Мы не собираемся опять проходить весь процесс создания нового изменения и его извлечения, но мы хотим, чтобы вы знали, что выполнение:</p>

<pre class="instructions">git pull</pre>

<p>действительно эквивалентно двум следующим шагам:</p>

<pre class="instructions">git fetch
git merge origin/master</pre>