---
view: page
title: "48. Відправка змін"
---

<h3>Цілі</h3>

<ul><li>Навчитися відправляти зміни в віддалений репозиторій.</li></ul>

<p>Так як чисті репозиторії, як правило, расшаріваються на якому-небудь мережевому сервері, нам необхідно відправити наші зміни до інших репозиторіїв.</p>

<p>Почнемо зі створення змін для відправки. Відредагуйте файл <span class="caps">README</span> і зробіть коміт</p>

<h4 class="h4-pre"> Файл: <em><span class="caps"> README </span></em></h4>

<pre class="file">This is the Hello World example from the git tutorial.
(Changed in the original and pushed to shared)</pre>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added shared comment to readme"</pre>

<p>Тепер надішліть зміни до загального репозиторію.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git push shared master</pre>

<p><em>Загальним</em> називається репозиторій, який одержує відправлені нами зміни. (Пам'ятаєте, ми додали його в якості віддаленого репозиторію в попередньому уроці.)</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git push shared master
To ../hello.git
   2faa4ea..79f507c  master -&gt; master</pre>

<p class="note"><strong><span class="caps">Примітка</span>:</strong> Ми повинні були явно вказати гілку master для відправки змін. Це можна налаштувати автоматично, але я весь час забуваю потрібні команди. Для більш простого управління віддаленими гілками переключіться в «Git Remote Branch».</p>