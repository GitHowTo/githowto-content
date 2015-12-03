---
view: page
title: "12. Отримання старих версій"
---

<h3>Цілі</h3>

<ul><li>Навчитися повертати робочий каталог до будь-якого попереднього стану.</li></ul>

<p>Повертатися назад в історію дуже просто. Команда checkout скопіює будь-який знімок з репозиторію в робочий каталог.</p>

<h2><em>01</em> Отримайте хеши попередніх версій</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git hist</pre>

<p class="note"><strong>Примітка:</strong> Ви не забули задати <code>hist</code> у вашому файлі <code>.gitconfig</code>? Якщо забули, подивіться ще раз урок по <a href="/aliases">алиасах</a>.</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Вивчіть дані логу і знайдіть хеш для першого коміту. Він повинен бути в останньому рядку даних <code>git hist</code>. Використовуйте цей хеш-код (досить перших 7 знаків) в команді нижче. Потім перевірте вміст файлу <code>hello.html</code>.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout &lt;hash&gt;
cat hello.html</pre>

<p class="note"><strong>Примітка:</strong> Багато команд залежать від хешевих значень в репозиторії. Оскільки ваші хеш-значення будуть відрізнятися від моїх, коли ви бачите щось на зразок <code>&lt;hash&gt;</code> чи <code>&lt;treehash&gt;</code> у команді, підставте необхідне значення хешу для вашого репозітарію.</p>

<p>Ви побачите…</p>

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

<p>Вихідні дані команди <code>checkout</code> дуже добре пояснюють ситуацію. Старі версії git будуть лаятися, що не налаштовані в локальній гілці. У будь-якому разі, зараз про це не турбуйтеся.</p>

<p>Зверніть увагу на те, що вміст файлу hello.html є значенням за замовчуванням.</p>

<h2><em>02</em> Поверніться до останньої версії в гілці master </h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout master
cat hello.html</pre>

<p>Ви побачите…</p>

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

<p>«master» — ім'я гілки за замовчуванням. Перемикаючи імена гілок, ви потрапляєте на останню версію обраної гілки.</p>