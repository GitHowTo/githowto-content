---
view: page
title: "19. Внесення змін до комітів"
---

<h3>Цілі</h3>

<ul><li>Навчитися змінювати існуючі коміти</li></ul>

<h2><em>01</em> Змініть сторінку, а потім зробіть коміт</h2>

<p>Додайте в сторінку коментар автора.</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add hello.html
git commit -m "Add an author comment"</pre>

<h2><em>02</em> Ой... необхідний email</h2>

<p>Після скоєння коміту ви розумієте, що будь-який хороший коментар повинен включати електронну пошту автора. Оновіть сторінку hello, включивши в неї email.</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Змініть попередній коміт</h2>

<p>Ми дійсно не хочемо створювати окремий коміт тільки заради електронної пошти. Давайте змінимо попередній коміт, включивши в нього адресу електронної пошти.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add hello.html
git commit --amend -m "Add an author/email comment"</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git add hello.html
$ git commit --amend -m "Add an author/email comment"
[master 6a78635] Add an author/email comment
 1 files changed, 2 insertions(+), 1 deletions(-)</pre>

<h2><em>04</em> Перегляд історії</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist
* 6a78635 2011-03-09 | Add an author/email comment (HEAD, master) [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Ми можемо побачити, що оригінальний коміт «автор» замінений на коміт «автор/email». Цього ж ефекту можна досягти шляхом скидання останнього коміту в гілці, і повторного коміту нових змін.</p>