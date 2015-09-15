---
view: page
title: "41. Изменение оригинального репозитория"
---

<h3>Цели</h3>

<ul><li>Внести некоторые изменения в оригинальный репозиторий, чтобы затем попытаться извлечь и слить изменения из удаленной ветки в текущую</li></ul>

<h2><em>01</em> Внесите изменения в оригинальный репозиторий <strong>hello</strong></h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">cd ../hello
# (You should be in the original hello repository now)</pre>

<p style="color:red;"><strong><span class="caps">Примечание</span>: Сейчас мы находимся  в репозитории <em>hello</em> </strong></p>

<p>Внесите следующие изменения в файл <span class="caps">README</span>:</p>

<h4 class="h4-pre">Файл: <em><span class="caps">README</span></em></h4>

<pre class="file">This is the Hello World example from the git tutorial.
(changed in original)</pre>

<p>Теперь добавьте это изменение и сделайте коммит</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add README
git commit -m "Changed README in original repo"</pre>

<h2><em>02</em> Далее</h2>

<p>Теперь в оригинальном репозитории есть более поздние изменения, которых нет в клонированной версии. Далее мы извлечем и сольем эти изменения в клонированный репозиторий.</p>