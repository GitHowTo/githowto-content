---
view: page
title: "12. Usando vers&otilde;es anteriores"
---

<h3>Metas</h3>

<ul><li>Aprender como aplicar qualquer snapshot anterior ao diret&oacute;rio de trabalho.</li></ul>

<p>Voltar no hist&oacute;rico &eacute; bem simples. O comando checkout pode copiar qualquer snapshot do reposit&oacute;rio para o diret&oacute;rio de trabalho.</p>

<h2><em>01</em> Conseguindo os hashes das vers&otilde;es anteriores</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist</pre>

<p class="note"><strong>Nota:</strong> N&atilde;o esque&ccedil;a de definir o alias <code>hist</code> no seu arquivo <code>.gitconfig</code>. Se voc&ecirc; n&atilde;o lembra como fazer isso, reveja a li&ccedil;&atilde;o sobre aliases.</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Confira a data do log e encontre o hash do primeiro commit. Voc&ecirc; vai achar ele na &uacute;ltima linha do <code>git hist</code> Use o c&oacute;digo (os seus 7 primeiros caracteres s&atilde;o suficientes) no comando abaixo. Depois disso, cheque o conte&uacute;do do arquivo hello.html.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout &lt;hash&gt;
cat hello.html</pre>

<p class="note"><strong>Nota:</strong> V&aacute;rios comandos dependem dos valores de hash do reposit&oacute;rio. J&aacute; que os meus valores de hash ser&atilde;o diferentes dos seus, fa&ccedil;a as substitui&ccedil;&otilde;es apropriadas no seu hash do reposit&oacute;rio todas as vezes que voc&ecirc; ver <code>&lt;hash&gt;</code> ou <code>&lt;treehash&gt;</code> no comando.</p>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout 911e8c9
Note: checking out '911e8c9'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 911e8c9... First Commit
$ cat hello.html
Hello, World</pre>

<p>O resultado do comando <code>checkout</code> esclarece completamente a situa&ccedil;&atilde;o. Vers&otilde;es mais antigas do git v&atilde;o reclamar sobre n&atilde;o estarem em um branch local. Mas voc&ecirc; n&atilde;o precisa de preocupar com isso agora.</p>

<p>Perceba que o conte&uacute;do do arquivo hello.html &eacute; o conte&uacute;do padr&atilde;o.</p>

<h2><em>02</em> Voltando para a vers&atilde;o mais atual no branch master</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
cat hello.html</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout master
Previous HEAD position was 911e8c9... First Commit
Switched to branch 'master'
$ cat hello.html
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

<p>&#8216;master&#8217; &eacute; o nome do branch padr&atilde;o. Ao entrar em um branch pelo seu nome, voc&ecirc; vai para a sua vers&atilde;o mais atual.</p>
