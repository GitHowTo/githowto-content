---
view: page
title: "8. Коммит изменений"
---

<h3>Цели</h3>

<ul><li>Научиться коммитить изменения в репозиторий</li></ul>

<h2><em>01</em> Закоммитьте изменения</h2>

<p>Достаточно об индексации. Давайте сделаем коммит того, что мы проиндексировали, в репозиторий.</p>

<p>Когда вы ранее использовали <code>git commit</code> для коммита первоначальной версии файла <code>hello.html</code> в репозиторий, вы включили метку <code>-m</code>, которая делает комментарий в командной строке. Команда commit позволит вам интерактивно редактировать комментарии для коммита. Теперь давайте это проверим.</p>

<p>Если вы опустите метку <code>-m</code> из командной строки, git перенесет вас в редактор по вашему выбору. Редактор выбирается из следующего списка (в порядке приоритета):</p>

<ul>
<li>переменная среды <span class="caps">GIT_EDITOR</span></li>
<li>параметр конфигурации core.editor</li>
<li>переменная среды <span class="caps">VISUAL</span></li>
<li>переменная среды <span class="caps">EDITOR</span></li>
</ul>

<p>У меня переменная <span class="caps">EDITOR</span> установлена в <code>emacsclient</code> (доступен для Linux и Mac).</p>

<p>Сделайте коммит сейчас и проверьте состояние.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git commit</pre>

<p>Вы увидите в вашем редакторе:</p>

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

<p>В первой строке введите комментарий: «Added h1 tag». Сохраните файл и выйдите из редактора (для этого в редакторе по-умолчанию (Vim) вам нужно нажать клавишу ESC, ввести <code>:wq</code> и нажать Enter). Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">git commit
Waiting for Emacs...
[master 569aa96] Added h1 tag
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>Строка «Waiting for Emacs…» получена из программы <code>emacsclient</code>, которая посылает файл в запущенную программу emacs и ждет его закрытия. Остальные выходные данные – стандартные коммит-сообщения.</p>

<h2><em>02</em> Проверьте состояние</h2>

<p>В конце давайте еще раз проверим состояние.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git status</pre>

<p>Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>Рабочий каталог чистый, можете продолжить работу.</p>