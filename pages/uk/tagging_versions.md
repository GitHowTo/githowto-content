---
view: page
title: "13. Створення тегів версій"
---

<h3>Цілі</h3>

<ul><li>Дізнатися, як створювати теги для коммітов для використання в майбутньому</li></ul>

<p>Давайте назвемо поточну версію сторінки hello першою (<em>v1</em>).</p>

<h2><em>01</em> Створіть тег першої версії</h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git tag v1</pre>

<p>Тепер поточна версія сторінки називається <em>v1</em>.</p>

<h2><em>02</em> Теги для попередніх версій </h2>

<p>Давайте створимо тег для версії, яка йде перед поточною версією і назвемо його <em>v1-beta</em>. У першу чергу нам треба переключитися на попередню версію. Замість пошуку по хешу, ми будемо використовувати <code>^</code>, що означає «родитель v1».</p>

<p class="note">Якщо позначення <code>v1^</code> викликає у вас якісь проблеми, спробуйте також <code>v1~1</code>, яке вказує на ту саму версію. Це позначення можна визначити як «першу версію попередню v1».</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout v1^
cat hello.html</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout v1^
Note: checking out 'v1^'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 8c32287... Added standard HTML page tags
$ cat hello.html
&lt;html&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Це версія з тегами <code>&lt;html&gt;</code> та <code>&lt;body&gt;</code>, але <em>поки що</em> без  <code>&lt;head&gt;</code>. Давайте зробимо її версією <em>v1-beta</em>.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git tag v1-beta</pre>

<h2><em>03</em> Перемикання за ім'ям тегу </h2>

<p>Тепер спробуйте попереключатися між двома зазначеними версіями.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout v1
git checkout v1-beta</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout v1
Previous HEAD position was 8c32287... Added standard HTML page tags
HEAD is now at fa3c141... Added HTML header
$ git checkout v1-beta
Previous HEAD position was fa3c141... Added HTML header
HEAD is now at 8c32287... Added standard HTML page tags</pre>

<h2><em>04</em> Перегляд тегів за допомогою команди <code>tag</code></h2>

<p>Ви можете побачити, які теги доступні, використовуючи команду <code>git tag</code>.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git tag</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git tag
v1
v1-beta</pre>

<h2><em>05</em> Перегляд тегів у логах </h2>

<p>Ви також можете подивитися теги у лозі.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git hist master --all</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist master --all
* fa3c141 2011-03-09 | Added HTML header (v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (HEAD, v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Ви можете бачити теги(<code>v1</code> и <code>v1-beta</code>) у лозі разом з ім'ям гілки(<code>master</code>). Крім того <code>HEAD</code> показує коміт, на який ви переключилися (зараз це <code>v1-beta</code>).</p>