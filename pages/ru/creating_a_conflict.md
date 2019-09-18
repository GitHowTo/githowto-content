---
view: page
title: "29. Создание конфликта"
---

<h3>Цели</h3>

<ul><li>Создание конфликтующих изменений в ветке master.</li></ul>

<h2><em>01</em> Вернитесь в master и создайте конфликт</h2>

<p>Вернитесь в ветку master и внесите следующие изменения:</p>

<pre class="instructions">git checkout master</pre>

<h4 class="h4-pre">Файл: <em style="text-transform: none">lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- no style --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World! <strong>Life is great!</strong>&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m 'Life is great!'</pre>

<b>Внимание:</b> используйте для этого коммита одинарные кавычки, дабы избежать проблем с символом <code>!</code>. В bash он считается служебным.

<h2><em>02</em> Просмотр веток</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist --all
* 454ec68 2011-03-09 | Life is great! (HEAD, master) [Alexander Shvets]
| * 5813a3f 2011-03-09 | Merge branch 'master' into style (style) [Alexander Shvets]
| |\  
| |/  
|/| 
* | 6c0f848 2011-03-09 | Added README [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html [Alexander Shvets]
| * 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
| * 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>После коммита «Added <span class="caps">README</span>» ветка master была объединена с веткой style, но в настоящее время в master есть дополнительный коммит, который не был  слит с style.</p>

<h2><em>03</em> Далее</h2>

<p>Последнее изменение в master конфликтует с некоторыми изменениями в style. На следующем шаге мы решим этот конфликт.</p>
