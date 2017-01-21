---
view: page
title: "11. Псевдоніми"
---

<h3>Цілі</h3>

<ul><li>Навчитися налаштовувати псевдоніми і скорочені шляхи для команд git</li></ul>

<h2><em>01</em> Загальні псевдоніми</h2>

<p>Для користувачів Windows:</p>
<h4 class="h4-pre">Виконати:</h4>
<pre class="instructions">git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.br branch
git config --global alias.hist "log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short"
git config --global alias.type 'cat-file -t'
git config --global alias.dump 'cat-file -p'</pre>

<p>Також, для користувачів Unix/Mac:</p>
<p><ins>git status</ins>, <ins>git add</ins>, <ins>git commit</ins>, <ins>git checkout</ins> — загальні команди, для котрих корисно мати скорочення.</p>

<p>Додайте наступне у файл .gitconfig у вашому $<span class="caps">HOME</span> каталозі.</p>

<h4 class="h4-pre">Файл: <em>.gitconfig</em></h4>

<pre class="file">[alias]
  co = checkout
  ci = commit
  st = status
  br = branch
  hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
  type = cat-file -t
  dump = cat-file -p</pre>

<p>Ми вже встигли розібрати команди <code>commit</code> та <code>status</code>, у попередньому уроці вивчили команду <code>log</code> і зовсім скоро познайомимось з <code>checkout</code>. Головне, що варто запам'ятати з цього уроку, це те, що тепер ви можете вводити <code>git st</code> там, де раніше мали набирати <code>git status</code>. Аналогічно, пишемо <code>git co</code> замість <code>git checkout</code> та <code>git ci</code> замість <code>git commit</code>. Найкраще те, що команда <code>git hist</code> дозволить уникнути введення довжелезної команди <code>log</code>.</p>

<p>Спробуйте використовувати нові команди.</p>

<h2><em>02</em> Задайте псевдонім <code>hist</code> у файлі <code>.gitconfig</code> </h2>

<p>Здебільшого, я буду продовжувати використовувати повні команди у цьому керівництві. Єдиним виключенням буде використання псевдоніму <code>hist</code>, згаданого вище, коли мені знадобиться подивитися git лог. Якщо ви хочете повторювати мої дії, переконайтеся, що псевдонім <code>hist</code> встановлено у вашому файлі <code>.gitconfig</code>.</p>

<h2><em>03</em> <code>Type</code> та <code>Dump</code></h2>

<p>Ми додали кілька псевдонімів для команд, котрі ми ще не торкалися. З командою <code>git branch</code> розберемося трохи пізніше, а команду <code>git cat-file</code> використовується для дослідження git, у цьому ми невдовзі переконаємось.</p>

<h2><em>04</em> Псевдоніми команд (опціонально)</h2>

<p>Якщо ваша оболонка підтримує псевдоніми чи скорочені шляхи, ви можете додавати псевдоніми і на цьому рівні. Я користуюся:</p>

<h4 class="h4-pre">Файл: <em>.profile</em></h4>

<pre class="file">alias gs='git status '
alias ga='git add '
alias gb='git branch '
alias gc='git commit'
alias gd='git diff'
alias go='git checkout '
alias gk='gitk --all&amp;'
alias gx='gitx --all'

alias got='git '
alias get='git '</pre>

<p>Скорочення <code>go</code> для команди <code>git checkout</code> особливо корисне. Воно дозволяє мені вводити:</p>

<pre class="instructions">go &lt;branch&gt;</pre>

<p>для переходу в окрему гілку.</p>

<p>І так, я достатньо часто пишу замість <code>git</code> <code>get</code> чи <code>got</code>, тому створю псевдоніми й для них.</p>
