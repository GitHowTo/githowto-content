---
view: page
title: "44. Витяг і злиття змін"
---

<h3>Цілі</h3>

<ul><li>Дізнатися про те, що команда <code>git pull</code> еквівалентна комбінації <code>git fetch</code> і <code>git merge</code>.</li></ul>

<h3> Обговорення </h3>

<p>Ми не збираємося знову проходити весь процес створення нових змін та їх вилучення, але ми хочемо, щоб ви знали, що виконання:</p>

<pre class="instructions">git pull</pre>

<p>дійсно еквівалентно двом наступним крокам:</p>

<pre class="instructions">git fetch
git merge origin/master</pre>