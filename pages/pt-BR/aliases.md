---
view: page
title: "11. Aliases"
---

<h3>Metas</h3>

<ul><li>Aprender como configurar aliases e atalhos para comandos do git</li></ul>

<h2><em>01</em> Aliases comuns</h2>

<p>Para usu&aacute;rios do Windows:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.br branch
git config --global alias.hist 'log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short'
git config --global alias.type 'cat-file -t'
git config --global alias.dump 'cat-file -p'</pre>

<p>Al&eacute;m disso, para usu&aacute;rios de Unix/Mac:</p>

<p><ins>git status</ins>, <ins>git add</ins>, <ins>git commit</ins>, e <ins>git checkout</ins> s&atilde;o comandos comuns, ent&atilde;o &eacute; uma boa ideia ter abrevia&ccedil;&otilde;es para eles.</p>

<p>Adicione o seguinte no arquivo <code>.gitconfig</code> no seu diret&oacute;rio <code>$<span class="caps">HOME</span></code>.</p>

<h4 class="h4-pre">Arquivo: <em>.gitconfig</em></h4>

<pre class="file">[alias]
  co = checkout
  ci = commit
  st = status
  br = branch
  hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
  type = cat-file -t
  dump = cat-file -p</pre>

<p>N&oacute;s j&aacute; falamos sobre os comandos commit e status. Nas li&ccedil;&otilde;es anteriores, n&oacute;s cobrimos o comando <code>log</code> e vamos conhecer o comando checkout em breve. O mais importante a se aprender dessa li&ccedil;&atilde;o &eacute; que voc&ecirc; pode digitar <code>git st</code> onde voc&ecirc; antes tinha que digitar <code>git status</code>. O melhor de tudo &eacute; que o comando <code>git hist</code> evita que voc&ecirc; precise do comando <code>log</code>, que &eacute; muito comprido.</p>

<p>V&aacute; em frente e teste os novos comandos.</p>

<h2><em>02</em> Defina o alias <code>hist</code> no arquivo .gitconfig</h2>

<p>Na maioria das vezes, eu vou continuar a escrever o comando completo nessas instru&ccedil;&otilde;es. A &uacute;nica exce&ccedil;&atilde;o vai ser o alias <code>hist</code> definido acima, que eu vou usar quando precisar de verificar o git log. Tenha certeza que voc&ecirc; tem um <code>hist</code> alias configurado em seu arquivo <code>.gitconfig</code> antes de continuar se voc&ecirc; deseja repetir minhas a&ccedil;&otilde;es.</p>

<h2><em>03</em> <code>Type</code> e <code>Dump</code></h2>

<p>N&oacute;s adicionamos alguns aliases para comandos que n&oacute;s ainda n&atilde;o discutimos. N&oacute;s vamos falar sobre o comando <code>git branch</code> em breve, e o comando <code>git cat-file</code> &eacute; muito &uacute;til para explorar o git.</p>

<h2><em>04</em> Aliases de comandos (opcional)</h2>

<p>Se sua shell suporta aliases ou atalhos, voc&ecirc; pode adicion&aacute;-los por l&aacute; tamb&eacute;m. Eu uso:</p>

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

<p>A abrevia&ccedil;&atilde;o <code>gco</code> para <code>git checkout</code> &eacute; muito &uacute;til, pois me permite digitar:</p>

<pre class="instructions">gco &lt;branch&gt;</pre>

<p>para mudar para um branch em espec&iacute;fico.</p>

<p>Al&eacute;m disso, eu costumo digitar <code>get</code> ou <code>got</code> quando vou digitar <code>git</code>, ent&atilde;o criei aliases para eles tamb&eacute;m.</p>
