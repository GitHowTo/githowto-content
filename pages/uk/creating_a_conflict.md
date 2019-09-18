---
view: page
title: "29. Створення конфлікту"
---

<h3>Цілі</h3>

<ul><li>Створення конфліктуючих змін в гілці master.</li></ul>

<h2><em>01</em> Поверніться у master і створіть конфлікт</h2>

<p>Поверніться у гілку master і внесіть такі зміни:</p>

<pre class="instructions">git checkout master</pre>

<h4 class="h4-pre">Файл: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- no style --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World! <strong>Life is great!</strong>&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Виконайте</h4>

<pre class="instructions">git add lib/hello.html
git commit -m 'Life is great!'</pre>

<b>Увага:</b> використовуйте для цього коміту одинарні лапки, щоб уникнути проблем з символом <code>!</code>. У bash він вважається службовим.

<h2><em>02</em> Перегляд гілок</h2>

<h4 class="h4-pre">Виконайте:</h4>

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

<p>Після коміту «Added <span class="caps">README</span>» гілка master була об'єднана з гілкою style, але в даний час в master є додатковий коміт, який не був злитий зі  style.</p>

<h2><em>03</em> Далі</h2>

<p>Остання зміна в master конфліктує з деякими змінами в style. У наступному кроці ми вирішимо цей конфлікт.</p>