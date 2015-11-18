---
view: page
title: "16. Скасування комітів"
---

<h3>Цілі</h3>

<ul><li>Навчитися скасовувати коміти до локального репозиторію.</li></ul>

<h2><em>01</em> Скасування комітів</h2>

<p>Іноді ви розумієте, що нові коміти є невірними, і хочете їх скасувати. Є кілька способів вирішення цього питання, тут ми будемо використовувати найбезпечніший.</p>

<p>Ми скасуємо коміт шляхом створення нового коміту, що скасовує небажані зміни.</p>

<h2><em>02</em> Змініть файл і зробіть коміт</h2>

<p>Змініть файл <code>hello.html</code> на наступний.</p>

<h4 class="h4-pre">Файл: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is an unwanted but committed change --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add hello.html
git commit -m "Oops, we didn't want this commit"</pre>

<h2><em>03</em> Зробіть коміт з новими змінами, скасовуючими попередні </h2>

<p>Щоб скасувати коміт, нам необхідно зробити коміт, який видаляє зміни, збережені небажаним коміом.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git revert HEAD</pre>

<p>Перейдіть у редактор, де ви можете відредагувати коміт-повідомлення за замовчуванням або залишити все як є. Збережіть і закрийте файл. Ви побачите…</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git revert HEAD --no-edit
[master 45fa96b] Revert "Oops, we didn't want this commit"
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>Так як ми скасували самий останній коміт, ми змогли використати  <code>HEAD</code> в якості аргументу для скасування. Ми можемо скасувати будь-який довільний коміт в історії, вказавши його хеш-значення.</p>

<p class="note"><strong>Примітка:</strong> Команду <code>--no-edit</code> можна проігнорувати. Вона була необхідна для генерації вихідних даних без відкриття редактора.</p>

<h2><em>04</em> Перевірте лог</h2>

<p>Перевірка логу показує небажані та скасовані коміти до нашого репозиторію.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (HEAD, master) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Ця техніка працюватиме з будь-яким комітом (хоча, можливо, виникнуть конфлікти). Вона безпечна у використанні навіть у публічних гілках віддалених репозиторіїв.</p>

<h2><em>05</em> Далі</h2>

<p>Далі давайте подивимося на техніку, яка може бути використана для видалення останніх комітів з історії репозиторію.</p>