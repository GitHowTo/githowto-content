---
view: page
title: "1. Подготовка"
---

<h3>Цели</h3>

<ul><li>Полная готовность к работе с Git.</li></ul>

<h2><em>01</em> Установка имени и электронной почты</h2>

<p>Если вы никогда ранее не использовали git, для начала вам необходимо осуществить установку. Выполните следующие команды, чтобы git узнал ваше имя и электронную почту. Если git уже установлен, можете переходить к разделу <a href="http://ru.wikipedia.org/wiki/%D0%9F%D0%B5%D1%80%D0%B5%D0%B2%D0%BE%D0%B4_%D1%81%D1%82%D1%80%D0%BE%D0%BA%D0%B8">окончания строк</a>.</p>

<h4 class="h4-pre">Выполнить:</h4>

<pre class="instructions">git config --global user.name "Your Name"
git config --global user.email "your_email@whatever.com"</pre>

<h2><em>02</em> Параметры установки окончаний строк</h2>

<p>Также, для пользователей Unix/Mac:</p>

<h4 class="h4-pre">Выполнить:</h4>

<pre class="instructions">git config --global core.autocrlf input
git config --global core.safecrlf true</pre>

<p>Для пользователей Windows:</p>

<h4 class="h4-pre">Выполнить:</h4>

<pre class="instructions">git config --global core.autocrlf true
git config --global core.safecrlf true</pre>