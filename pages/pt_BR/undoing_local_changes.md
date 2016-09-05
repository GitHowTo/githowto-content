---
view: page
title: "14. Descartando mudan&ccedil;as locais (antes do stage)"
---

<h3>Metas</h3>

<ul><li>Aprender como descartar mudan&ccedil;as no reposit&oacute;rio de trabalho</li></ul>

<h2><em>01</em> Acessando o branch Master</h2>

<p>Verifique que voc&ecirc; esta no &uacute;ltimo commit do branch master antes de continuar.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master</pre>

<h2><em>02</em> Mude o hello.html </h2>

<p>Acontece de voc&ecirc; modificar o arquivo no seu diret&oacute;rio de trabalho local e &agrave;s vezes querer descartar as mudan&ccedil;as que voc&ecirc; fez commit. &Eacute; aqui que o comando checkout vai te ajudar.</p>

<p>Fa&ccedil;a mudan&ccedil;as ao arquivo hello.html na forma de um coment&aacute;rio indesejado.</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is a bad comment.  We want to revert it. --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Confira o status</h2>

<p>Primeiro de tudo, confira o status do reposit&oacute;rio de trabalho.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

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

<p>N&oacute;s vemos que o arquivo <code>hello.html</code> foi modificado, mas ainda n&atilde;o est&aacute; no stage.</p>

<h2><em>04</em> Desfazendo as mudan&ccedil;as no diret&oacute;rio de trabalho</h2>

<p>Use o comando <code>checkout</code> para remover a vers&atilde;o do arquivo <code>hello.html</code> que est&aacute; no reposit&oacute;rio.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout hello.html
git status
cat hello.html</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout hello.html
$ git status
# On branch master
nothing to commit (working directory clean)
$ cat hello.html
&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>O comando status mostra que n&atilde;o existem mudan&ccedil;as que n&atilde;o est&atilde;o no stage no reposit&oacute;rio de trabalho. E o &#8220;coment&aacute;rio ruim&#8221; n&atilde;o est&aacute; mais no arquivo.</p>
