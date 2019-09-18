---
view: page
title: "26. Изменения в ветке master"
---

<h3>Цели</h3>

<ul><li>Научиться работать с несколькими ветками с различными (и, возможно, конфликтующими) изменениями.</li></ul>

<p>Пока вы меняли ветку «style», кто-то решил обновить ветку master. Они добавили <span class="caps">README</span>.</p>

<h2><em>01</em> Создайте файл <span class="caps">README</span> в ветке master.</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout master</pre>

<h4 class="h4-pre">Файл: <em><span class="caps">README</span></em></h4>

<pre class="file">This is the Hello World example from the git tutorial.</pre>

<h2><em>02</em> Сделайте коммит изменений <span class="caps">README</span> в ветку master.</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add README
git commit -m "Added README"</pre>
