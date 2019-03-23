---
view: page
title: "12. Получение старых версий"
---

<h3>Цели</h3>

<ul><li>Научиться возвращать рабочий каталог к любому предыдущему состоянию.</li></ul>

<p>Возвращаться назад в историю очень просто. Команда checkout скопирует любой снимок из репозитория в рабочий каталог.</p>

<h2><em>01</em> Получите хэши предыдущих версий</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist</pre>

<p class="note"><strong>Примечание:</strong> Вы не забыли задать <code>hist</code> в вашем файле <code>.gitconfig</code>? Если забыли, посмотрите еще раз урок по <a href="/ru/aliases">алиасам</a>.</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Изучите данные лога и найдите хэш для первого коммита. Он должен быть в последней строке данных <code>git hist</code>. Используйте этот хэш-код (достаточно первых 7 знаков) в команде ниже.  Затем проверьте содержимое файла <code>hello.html</code>.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout &lt;hash&gt;
cat hello.html</pre>

<p class="note"><strong>Примечание:</strong> Многие команды зависят от хэшевых значений в репозитории. Поскольку ваши хеш-значения будут отличаться от моих, когда вы видите что-то вроде <code>&lt;hash&gt;</code> или <code>&lt;treehash&gt;</code> в команде, подставьте необходимое значение хэш для вашего репозитория.</p>

<p>Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout 911e8c9
Note: checking out '911e8c9'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 911e8c9... First Commit
$ cat hello.html
Hello, World</pre>

<p>Выходные данные команды <code>checkout</code> очень хорошо объясняют ситуацию. Старые версии git будут ругаться, что не расположены в локальной ветке. В любом случае, сейчас об этом не беспокойтесь.</p>

<p>Обратите внимание на то, что содержимое файла hello.html является значением по умолчанию.</p>

<h2><em>02</em> Вернитесь к последней версии в ветке master </h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout master
cat hello.html</pre>

<p>Вы увидите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout master
Previous HEAD position was 911e8c9... First Commit
Switched to branch 'master'
$ cat hello.html
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

<p>«master» — имя ветки по умолчанию. Переключая имена веток, вы попадаете на последнюю версию выбранной ветки.</p>