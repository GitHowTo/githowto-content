---
view: page
title: "8. Коміт змін"
---

<h3>Цілі</h3>

<ul><li>Навчитися комітити зміни у репозиторій</li></ul>

<h2><em>01</em>Закомітьте змини</h2>

<p>Досить про індексацію. Давайте зробимо коміт того, що ми проіндексували, у репозиторій.</p>

<p>Коли ви ранішу використовували <code>git commit</code> для коміту первинної версії файлу <code>hello.html</code> у репозиторій, ви включили мітку <code>-m</code>, яка робить коментар у командному рядку. Команда commit дозволить вам інтерактивно редагувати коментарі для коміту. Тепер давайте це перевіремо.</p>

<p>Якщо ви опустите мітку <code>-m</code> з командного рядку, git перенесе вас у редактор за вашим вибором. Редактор обирається з наступного списку (в порядку приорітету):</p>

<ul>
<li>змінна середовища <span class="caps">GIT_EDITOR</span></li>
<li>параметр конфігурації core.editor</li>
<li>змінна середовища <span class="caps">VISUAL</span></li>
<li>змінна середовища <span class="caps">EDITOR</span></li>
</ul>

<p>В мене змінна <span class="caps">EDITOR</span> встановлена в <code>emacsclient</code> (доступний для Linux та Mac).</p>

<p>Зробіть коміт зараз і провірте стан.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git commit</pre>

<p>Ви побачите у вашому редакторі:</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">|
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>У першому рядку введіть коментар: «Added h1 tag». Збережіть файл й вийдіть з редактору(для цього у редакторі за замовченням (Vim) вам необхідно натиснути клавішу ESC, ввести <code>:wq</code> й натиснути Enter). Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">git commit
Waiting for Emacs...
[master 569aa96] Added h1 tag
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>Рядок «Waiting for Emacs…» отримано з програми <code>emacsclient</code>, яка посилає файл у запущену програму emacs й чекає його закриття. Інші вихідні дані – стандартні коммит-сповіщення.</p>

<h2><em>02</em>Перевірте стан</h2>

<p>Наприкінці давайте ще раз перевіримо стан.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git status</pre>

<p>Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>Робочий каталог чистий, можете продовжувати роботу.</p>