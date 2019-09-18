---
view: page
title: "41. Зміна оригінального репозиторію"
---

<h3>Цілі</h3>

<ul><li>Внести деякі зміни в оригінальний репозиторій, щоб потім спробувати витягти і злити зміни з віддаленої гілки в поточну</li></ul>

<h2><em>01</em> Внесіть зміни в оригінальний репозиторій <strong>hello</strong></h2>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">cd ../hello
# (Зараз ви повинні бути в оригінальному hello репозиторію)</pre>

<p style="color:red;"><strong><span class="caps">Примітка</span>: Зараз ми знаходимося в репозиторію <em>hello</em> </strong></p>

<p>Внесіть наступні зміни у файл <span class="caps">README</span>:</p>

<h4 class="h4-pre">Файл: <em><span class="caps">README</span></em></h4>

<pre class="file">This is the Hello World example from the git tutorial.
(changed in original)</pre>

<p>Тепер додайте цю зміну і зробіть коміт</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git add README
git commit -m "Changed README in original repo"</pre>

<h2><em>02</em> Далі</h2>

<p>Тепер в оригінальному репозиторію є більш пізні зміни, яких немає в клонованій версії. Далі ми винесемо і зіллємо ці зміни до клонованого репозиторію.</p>