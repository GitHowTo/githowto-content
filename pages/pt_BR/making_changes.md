---
view: page
title: "5. Fazendo modifica&ccedil;&otilde;es"
---

<h3>Metas</h3>

<ul><li>Aprender a monitorar o estado do dir&eacute;torio de trabalho</li></ul>

<h2><em>01</em> Modificar a p&aacute;gina de “Hello, World”</h2>

<p>Vamos adicionar algumas tags HTML para a nossa sauda&ccedil;&atilde;o. Modifique os conte&uacute;dos do arquivo para:</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;h1&gt;</strong>Hello, World!<strong>&lt;/h1&gt;</strong></pre>

<h2><em>02</em> Conferindo o status</h2>

<p>Confira o status do diret&oacute;rio de trabalho.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>O primeiro aspecto importante aqui &eacute; que o git sabe que o arquivo <code>hello.html</code> foi modificado, mas essas modifica&ccedil;&otilde;es ainda n&atilde;o sofreram commit para o reposit&oacute;rio.</p>

<p>Outro aspecto &eacute; que a mensagem de status oferece dicas sobre o que fazer em seguida. Se voc&ecirc; quiser adicionar essas modifica&ccedil;&otilde;es para o reposit&oacute;rio, use <code>git add</code>. Para desfazer as modifica&ccedil;&otilde;es use <code>git checkout</code>.</p>

<h2><em>03</em> Pr&oacute;ximo...</h2>

<p>Colocando as modifica&ccedil;&otilde;es no stage.</p>
