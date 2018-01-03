---
view: page
title: "32. Скидання гілки style"
---

<h3>Цілі</h3>

<ul><li>Скидання гілки style до точки перед першим злиттям.</li></ul>

<h2><em>01</em> Скидання гілки style</h2>

<p> Давайте повернемося в часі у гілці style до точки <em>перед</em> тим, як ми злили її з гілкою master. Ми можемо <strong>скинути</strong> гілку до будь-якого коміту. По суті, це зміна покажчика гілки на будь-яку точку дерева комітів.</p>

<p>У цьому випадку ми хочемо повернутися в гілці style в точку перед злиттям з  master. Нам необхідно знайти останній коміт перед злиттям.</p>

<h4 class="h4-pre">Виконайте:</h4>

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

<p>Це трохи важко читати, але, дивлячись на дані, ми бачимо, що коміт «Updated index.html» був останнім у гілці style перед злиттям. Давайте скинемо гілку style до цього коміту.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git reset --hard &lt;hash&gt;</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git reset --hard 07a2a46
HEAD is now at 07a2a46 Updated index.html</pre>

<h2><em>02</em> Перевірте гілку.</h2>

<p>Пошукайте лог гілки style. У нас в історії більше немає комітів злиття.</p>

<h4 class="h4-pre">Виконайте:</h4>

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