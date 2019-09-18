---
view: page
title: "48. Отправка изменений"
---

<h3>Цели</h3>

<ul><li>Научиться отправлять изменения в удаленный репозиторий.</li></ul>

<p>Так как чистые репозитории, как правило, расшариваются на каком-нибудь сетевом сервере, нам необходимо отправить наши изменения в другие репозитории.</p>

<p>Начнем с создания изменения для отправки. Отредактируйте файл <span class="caps">README</span> и сделайте коммит</p>

<h4 class="h4-pre"> Файл: <em><span class="caps"> README </span></em></h4>

<pre class="file">This is the Hello World example from the git tutorial.
(Changed in the original and pushed to shared)</pre>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added shared comment to readme"</pre>

<p>Теперь отправьте изменения в общий репозиторий.</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git push shared master</pre>

<p><em>Общим</em> называется репозиторий, получающий отправленные нами изменения. (Помните, мы добавили его в качестве удаленного репозитория в предыдущем уроке.)</p>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git push shared master
To ../hello.git
   2faa4ea..79f507c  master -&gt; master</pre>

<p class="note"><strong><span class="caps">Примечание</span>:</strong>  Мы должны были явно указать ветку master для отправки изменений. Это можно настроить автоматически, но я все время забываю нужные команды. Для более простого управления удаленными ветками переключитесь в «Git Remote Branch».</p>