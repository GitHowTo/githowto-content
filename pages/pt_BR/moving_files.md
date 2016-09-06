---
view: page
title: "20. Movendo arquivos"
---

<h3>Metas</h3>

<ul><li>Aprender como mover um arquivo dentro do reposit&oacute;rio.</li></ul>

<h2><em>01</em> Mova o arquivo hello.html para a pasta <i>lib</i>.</h2>
<p>Agora criaremos a estrutura do nosso reposit&oacute;rio. Vamos mover a p&aacute;gina no diret&oacute;rio lib</p>
<h4 class="h4-pre">Execute:</h4>
<pre class="instructions">mkdir lib
git mv hello.html lib
git status</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ mkdir lib
$ git mv hello.html lib
$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	renamed:    hello.html -&gt; lib/hello.html
#</pre>

<p>Movendo arquivos com git, n&oacute;s notificamos o git sobre duas coisas</p>

<ol><li>O arquivo <code>hello.html</code> foi deletado.</li>
<li>O arquivo <code>lib/hello.html</code> foi criado.</li>
</ol><p>Ambos os fatos v&atilde;o para stage imediatamente e ficam prontos para o commit. O comando git status reporta que o arquivo foi movido.</p>

<h2><em>02</em> Mais um jeito de mover arquivos</h2>

<p>Um fato positivo sobre o git &eacute; que voc&ecirc; n&atilde;o precisa se lembrar de controle de vers&atilde;o no momento em que voc&ecirc; faz o commit do c&oacute;digo. O que poderia acontecer se n&oacute;s estiv&eacute;ssemos usando a linha de comando do sistema operacional ao inv&eacute;s do comando git para mover arquivos?</p>

<p>O pr&oacute;ximo set de comandos &eacute; id&ecirc;ntico &agrave;s nossas &uacute;ltimas a&ccedil;&otilde;es. &Eacute; necess&aacute;rio mais trabalho para o mesmo resultado.</p>

<p class="command"> N&oacute;s podemos fazer:</p>

<pre class="instructions">mkdir lib
mv hello.html lib
git add lib/hello.html
git rm hello.html</pre>

<h2><em>03</em> Fa&ccedil;a commit do novo diret&oacute;rio</h2>

<p>Vamos fazer commit dessa mudan&ccedil;a.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git commit -m "Moved hello.html to lib"</pre>
