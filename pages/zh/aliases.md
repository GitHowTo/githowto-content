---
view: page
title: "十一、别名"
---

<h3>目标</h3>

<ul><li>学会如何为git命令设置别名与快捷方式</li></ul>

<h2><em>01</em> 一些常用的别名</h2>

<p>对Windows用户来说：</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.br branch
git config --global alias.hist "log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short"
git config --global alias.type 'cat-file -t'
git config --global alias.dump 'cat-file -p'</pre>

<p>对Unix/Mac用户来说：</p>

<p><ins>git status</ins>、<ins>git add</ins>、<ins>git commit</ins>以及<ins>git checkout</ins>都是一些常用的命令，因此为它们设置缩写别名是一个好主意。</p>

<p>将以下内容添加到<code>$<span class="caps">HOME</span></code>目录下的<code>.gitconfig</code>文件中。</p>

<h4 class="h4-pre">文件：<em>.gitconfig</em></h4>

<pre class="file">[alias]
  co = checkout
  ci = commit
  st = status
  br = branch
  hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
  type = cat-file -t
  dump = cat-file -p</pre>

<p>我们已经学习过提交（commit）和状态查看（status）命令。在之前的课程中，我们学习过<code>log</code>命令，并将很快学习分支切换命令（checkout）。在本课中所学的最重要的事情是在你需要使用<code>git status</code>命令的时候，你只需要输入<code>git st</code>即可。而其中最好的命令之一，<code>git hist</code>免去了你输入冗长的<code>log</code>命令参数之苦。</p>

<p>让我们直接动手来尝试一下这些新的命令。</p>

<h2><em>02</em> 在.gitconfig文件中定义<code>hist</code>别名。</h2>

<p>在本教程的大多数时间里，我将会继续使用命令的全称。唯一的例外是<code>hist</code>别名，每当我需要查看git历史记录时，我都会使用<code>hist</code>。如果你希望重复我的命令输入，请先确保你在<code>.gitconfig</code>文件中进行了<code>hist</code>别名的设置。</p>

<h2><em>03</em> <code>Type</code>和<code>Dump</code></h2>

<p>我们刚才添加了一些我们还未讨论过的别名。其中，我们很快便将会学习<code>git branch</code>命令，而<code>git cat-file </code>命令则对探索git很有帮助。</p>

<h2><em>04</em> 命令别名（可选的）</h2>

<p>如果你的shell支持别名或者快捷方式设置，你也可以在这一层面上添加一些别名。我使用以下这些：</p>

<h4 class="h4-pre">文件: <em>.profile</em></h4>

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

<p>其中的<code>go</code>是对<code>git checkout</code>的快捷简写方式，它允许我进行以下的输入：</p>

<pre class="instructions">go &lt;branch&gt;</pre>

<p>以切换至某个分支。</p>

<p>另外，我经常会将<code>git</code>误写成<code>get</code>或者<code>got</code>，所以我也为它们设置了别名。</p>
