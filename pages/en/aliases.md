---
view: page
title: "11. Aliases"
---

<h3>Goals</h3>

<ul><li>To learn how to setup aliases and shortcuts for git commands</li></ul>

<h2><em>01</em> Common aliases</h2>

<p>For Windows users:</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions">git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.br branch
git config --global alias.hist "log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short"
git config --global alias.type 'cat-file -t'
git config --global alias.dump 'cat-file -p'</pre>

<p>Also, for users of Unix/Mac:</p>

<p><ins>git status</ins>, <ins>git add</ins>, <ins>git commit</ins>, and <ins>git checkout</ins> are common commands so it is a good idea to have abbreviations for them.</p>

<p>Add the following to the <code>.gitconfig</code> file in your <code>$<span class="caps">HOME</span></code> directory.</p>

<h4 class="h4-pre">Файл: <em>.gitconfig</em></h4>

<pre class="file">[alias]
  co = checkout
  ci = commit
  st = status
  br = branch
  hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
  type = cat-file -t
  dump = cat-file -p</pre>

<p>We&#8217;ve already talked about commit and status  commands.  In the previous lesson we covered the <code>log</code> command and will get to know the checkout command very soon. The most important thing to learn from this lesson is that you can type <code>git st</code> wherever you had to type <code>git status</code>.  Best of all, the <code>git hist</code> command will help you avoid the really long <code>log</code> command.</p>

<p>Go ahead and try using the new commands.</p>

<h2><em>02</em> Define the <code>hist</code> alias in the .gitconfig file</h2>

<p>For the most part, I will continue to type out the full command in these instructions.  The only exception is that I will use the <code>hist</code> alias defined above, when I need to see the git log.  Make sure you have a <code>hist</code> alias setup in your <code>.gitconfig</code> file before continuing if you wish to repeat my actions.</p>

<h2><em>03</em> <code>Type</code> and <code>Dump</code></h2>

<p>We&#8217;ve added a few aliases for commands we haven&#8217;t yet discussed. We will talk about the <code>git branch</code> command very soon, and the <code>git cat-file</code> command is useful for exploring git.</p>

<h2><em>04</em> Command aliases (optional)</h2>

<p>If your shell supports aliases, or shortcuts, you can add aliases on this level, too. I use:</p>

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

<p>The <code>go</code> abbreviation for <code>git checkout</code> is very useful, allowing me to type:</p>

<pre class="instructions">go &lt;branch&gt;</pre>

<p>to checkout a particular branch.</p>

<p>Also, I often mistype <code>git</code> as <code>get</code> or <code>got</code> so I created aliases for them too.</p>