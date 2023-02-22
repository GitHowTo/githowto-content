---
view: page
title: "11. Aliases"
---

<h3>Metas</h3>

<ul><li>Aprender como configurar aliases e atalhos para comandos do git</li></ul>

<h2><em>01</em> Aliases comuns</h2>

<p>Para usuários do Windows:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.br branch
git config --global alias.hist 'log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short'
git config --global alias.type 'cat-file -t'
git config --global alias.dump 'cat-file -p'</pre>

<p>Além disso, para usuários de Unix/Mac:</p>

<p><ins>git status</ins>, <ins>git add</ins>, <ins>git commit</ins>, e <ins>git checkout</ins> são comandos comuns, então é uma boa ideia ter abreviações para eles.</p>

<p>Adicione o seguinte no arquivo <code>.gitconfig</code> no seu diretório <code>$<span class="caps">HOME</span></code>.</p>

<h4 class="h4-pre">Arquivo: <em>.gitconfig</em></h4>

<pre class="file">[alias]
  co = checkout
  ci = commit
  st = status
  br = branch
  hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
  type = cat-file -t
  dump = cat-file -p</pre>

<p>Nós já falamos sobre os comandos commit e status. Nas lições anteriores, nós cobrimos o comando <code>log</code> e vamos conhecer o comando checkout em breve. O mais importante a se aprender dessa lição é que você pode digitar <code>git st</code> onde você antes tinha que digitar <code>git status</code>. O melhor de tudo é que o comando <code>git hist</code> evita que você precise do comando <code>log</code>, que é muito comprido.</p>

<p>Vá em frente e teste os novos comandos.</p>

<h2><em>02</em> Defina o alias <code>hist</code> no arquivo .gitconfig</h2>

<p>Na maioria das vezes, eu vou continuar a escrever o comando completo nessas instruções. A única exceção vai ser o alias <code>hist</code> definido acima, que eu vou usar quando precisar de verificar o git log. Tenha certeza que você tem um <code>hist</code> alias configurado em seu arquivo <code>.gitconfig</code> antes de continuar se você deseja repetir minhas ações.</p>

<h2><em>03</em> <code>Type</code> e <code>Dump</code></h2>

<p>Nós adicionamos alguns aliases para comandos que nós ainda não discutimos. Nós vamos falar sobre o comando <code>git branch</code> em breve, e o comando <code>git cat-file</code> é muito útil para explorar o git.</p>

<h2><em>04</em> Aliases de comandos (opcional)</h2>

<p>Se sua shell suporta aliases ou atalhos, você pode adicioná-los por lá também. Eu uso:</p>

<h4 class="h4-pre">Arquivo: <em style="text-transform: none">.profile</em></h4>

<pre class="file">alias gs='git status'
alias ga='git add '
alias gb='git branch '
alias gc='git commit '
alias gd='git diff '
alias gco='git checkout '
alias gk='gitk --all&amp;'
alias gx='gitx --all '

alias got='git '
alias get='git '</pre>

<p>A abreviação <code>gco</code> para <code>git checkout</code> é muito útil, pois me permite digitar:</p>

<pre class="instructions">gco &lt;branch&gt;</pre>

<p>para mudar para um branch em específico.</p>

<p>Além disso, eu costumo digitar <code>get</code> ou <code>got</code> quando vou digitar <code>git</code>, então criei aliases para eles também.</p>
