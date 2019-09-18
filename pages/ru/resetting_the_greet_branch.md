---
view: page
title: "32. Сброс ветки style"
---

<h3>Цели</h3>

<ul><li>Сброс ветки style до точки перед первым слиянием.</li></ul>

<h2><em>01</em> Сброс ветки style</h2>

<p>Давайте вернемся во времени на ветке style к точке <em>перед</em> тем, как мы слили ее с веткой master. Мы можем <strong>сбросить</strong> ветку к любому коммиту. По сути, это изменение указателя ветки на любую точку дерева коммитов.</p>

<p>В этом случае мы хотим вернуться в ветке style в точку перед слиянием с master. Нам необходимо найти последний коммит перед слиянием.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout style
git hist</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout style
Already on 'style'
$ git hist
*   645c4e6 2011-03-09 | Merged master fixed conflict. (HEAD, style) [Alexander Shvets]
|\  
| * 454ec68 2011-03-09 | Life is great! (master) [Alexander Shvets]
* |   5813a3f 2011-03-09 | Merge branch 'master' into style [Alexander Shvets]
|\ \  
| |/  
| * 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* | 07a2a46 2011-03-09 | Updated index.html [Alexander Shvets]
* | 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
* | 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Это немного трудно читать, но, глядя на данные, мы видим, что коммит «Updated index.html» был последним на ветке style перед слиянием. Давайте сбросим ветку style к этому коммиту.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git reset --hard &lt;hash&gt;</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git reset --hard 07a2a46
HEAD is now at 07a2a46 Updated index.html</pre>

<h2><em>02</em> Проверьте ветку.</h2>

<p>Поищите лог ветки style. У нас в истории больше нет коммитов слияний.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist --all
* 454ec68 2011-03-09 | Life is great! (master) [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html (HEAD, style) [Alexander Shvets]
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