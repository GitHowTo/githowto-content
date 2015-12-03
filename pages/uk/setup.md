---
view: page
title: "1. Підготовка"
---

<h3>Цілі</h3>

<ul><li>Повна готовність до роботи з Git.</li></ul>

<h2><em>01</em> Встановлюємо ім'я та адресу електронної пошти</h2>

<p>Якщо ви ніколи раніше не використовували git, для початку вам необхідно здійснити установку. Виконайте наступні команди, щоб git дізнався про ваше ім'я та електронну пошту. Якщо git вже встановлено, можете переходити до розділу закінчення рядків.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git config --global user.name "Your Name"
git config --global user.email "your_email@whatever.com"</pre>

<h2><em>02</em> Параметри установки <a href="http://ru.wikipedia.org/wiki/%D0%9F%D0%B5%D1%80%D0%B5%D0%B2%D0%BE%D0%B4_%D1%81%D1%82%D1%80%D0%BE%D0%BA%D0%B8">закінчень рядків</a></h2>

<p>Також, для користувачів Unix/Mac:</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git config --global core.autocrlf input
git config --global core.safecrlf true</pre>

<p>Для користувачів Windows:</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git config --global core.autocrlf true
git config --global core.safecrlf true</pre>
