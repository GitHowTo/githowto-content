---
view: page
title: "9. Зміни, а не файли"
---

<h3>Цілі</h3>

<ul><li>Зрозуміти, що git працює зі змінами, а не файлами.</li></ul>

<p>Більшість систем версіонного контролю працюють з файлами. Ви додаєте файл в версіонний контроль і з цього моменту система відслідковує зміни файлу.</p>

<p>Git фокусується на змінах у файлі, а не на самому файлі. Коли ви виконуєте команду <code>git add file</code>,  ви не кажете git додати файл у репозиторій. Скоріше ви кажете, що git має відмітити поточний стан файлу, коміт якого буде виконано пізніше.</p>

<p>Ми спробуємо дослідити цю різницю в цьому уроці.</p>

<h2><em>01</em>Перша зміна: Додайте стандартні теги сторінок</h2>

<p>Змініть сторінку «Hello, World» так, щоб вона містила стандартні теги <code>&lt;html&gt;</code> й <code>&lt;body&gt;</code>.</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;html&gt;
  &lt;body&gt;</strong>
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  <strong>&lt;/body&gt;
&lt;/html&gt;</strong></pre>

<h2><em>02</em>Додайте ці зміни</h2>

<p>Тепер додайте ці зміни в індекс git.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>03</em>Друга зміна: Додайте заголовок HTML</h2>

<p>Тепер додайте заголовок HTML (секцію <code>&lt;head&gt;</code>) до сторінки «Hello, World».</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>04</em>Перевірте поточний статус</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git status</pre>

<p>Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#</pre>

<p>Зверніть увагу, що <code>hello.html</code> згадано двічі. Перша зміна(додавання стандартних тегів) проіндексирована і готова до коміту. Друга зміна(додавання заголовків HTML) є непроіндексована. Якщо б ви робили коміт зараз, заголовки не було б збережено у репозиторій.</p>

<p>Давайте перовіримо.</p>

<h2><em>05</em>Коміт</h2>

<p>Зробіть коміт проиндексованих змін(значення за замовченням), а потім ще раз перевірте стан.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git commit -m "Added standard HTML page tags"
git status</pre>

<p>Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git commit -m "Added standard HTML page tags"
[master 8c32287] Added standard HTML page tags
 1 files changed, 3 insertions(+), 1 deletions(-)
$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>Стан команди говорить про те, що <code>hello.html</code> має незафіксовані зміни, але вже не в буферній зоні.</p>

<h2><em>06</em>Додайте другу зміну</h2>

<p>Тепер додайте другу зміну в індекс, потім перевірте стан за допомогою команд <code>git status</code>.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add .
git status</pre>

<p class="note"><strong>Примітка:</strong>У якості файлу для додавання, ми використовували поточний каталог («.»). Це самий коротший й зручний шлях для додавання всіх змін у файли поточного каталогу й його підкаталогів. Але оскільки git додає все, <em>не зайвим</em> буде перевірити стан перед запуском <code>add</code>, просто щоб впевнетися, що ви не додали якийсь файл, який не треба було додавати.</p>

<p class="note">Я хотів показати вам трюк з <code>add</code>, надалі ми будемо про всяк випадок продовжувати додавати явні файли.</p>

<p>Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Другу зміну було проіндексовано й приготовлено до коміту.</p>

<h2><em>07</em>Зробіт коміт другою зміни</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git commit -m "Added HTML header"</pre>