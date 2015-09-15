---
view: page
title: "11. Алиасы"
---

<h3>Цели</h3>

<ul><li>Научиться настраивать алиасы и шорткаты для команд git</li></ul>

<h2><em>01</em> Общие алиасы</h2>

<p>Для пользователей Windows:</p>
<h4 class="h4-pre">Выполнить:</h4>
<pre class="instructions">git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.br branch
git config --global alias.hist 'log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short'
git config --global alias.type 'cat-file -t'
git config --global alias.dump 'cat-file -p'</pre>

<p>Также, для пользователей Unix/Mac:</p>
<p><ins>git status</ins>, <ins>git add</ins>, <ins>git commit</ins>, <ins>git checkout</ins> — общие команды, для которых полезно иметь сокращения.</p>

<p>Добавьте следующее в файл .gitconfig в вашем $<span class="caps">HOME</span> каталоге.</p>

<h4 class="h4-pre">Файл: <em>.gitconfig</em></h4>

<pre class="file">[alias]
  co = checkout
  ci = commit
  st = status
  br = branch
  hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
  type = cat-file -t
  dump = cat-file -p</pre>

<p>Мы уже успели рассмотреть команды <code>commit</code> и <code>status</code>, в предыдущем уроке рассмотрели команду <code>log</code> и совсем скоро познакомимся с <code>checkout</code>. Главное, что стоит запомнить из этого урока, так это то, что теперь вы можете вводить <code>git st</code> там, где раньше приходилось использовать <code>git status</code>. Аналогичным образом, пишем <code>git co</code> вместо <code>git checkout</code> и <code>git ci</code> вместо <code>git commit</code>. Что лучше всего, команда <code>git hist</code> позволит избежать ввода очень длинной команды <code>log</code>.</p>

<p>Попробуйте использовать новые команды.</p>

<h2><em>02</em> Задайте алиас <code>hist</code> в файле <code>.gitconfig</code> </h2>

<p>По большей части, я буду продолжать печатать полные команды в этом руководстве. Единственным исключением будет использование алиаса <code>hist</code>, указанного выше, когда мне понадобится посмотреть git лог. Если вы хотите повторять мои действия, убедитесь, что алиас <code>hist</code> установлен в вашем файле <code>.gitconfig</code>.</p>

<h2><em>03</em> <code>Type</code> и <code>Dump</code></h2>

<p>Мы добавили несколько алиасов для команд, которых мы еще не рассматривали. С командой <code>git branch</code> разберемся чуть позже, а команда <code>git cat-file</code> используется для исследования git, в чем мы вскоре убедимся.</p>

<h2><em>04</em> Алиасы команд (опционально)</h2>

<p>Если ваша оболочка поддерживает алиасы или шорткаты, вы можете добавить алиасы и на этом уровне. Я использую:</p>

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

<p>Сокращение <code>go</code> для команды <code>git checkout</code> особенно полезно. Оно позволяет мне вводить:</p>

<pre class="instructions">go &lt;branch&gt;</pre>

<p>для переключения в отдельную ветку.</p>

<p>И да, я достаточно часто пишу вместо <code>git</code> <code>get</code> или <code>got</code>, поэтому создам алиасы и для них.</p>