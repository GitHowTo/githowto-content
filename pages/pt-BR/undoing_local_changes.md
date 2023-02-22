---
view: page
title: "14. Descartando mudanças locais (antes do stage)"
---

<h3>Metas</h3>

<ul><li>Aprender como descartar mudanças no repositório de trabalho</li></ul>

<h2><em>01</em> Acessando o branch Master</h2>

<p>Verifique que você esta no último commit do branch master antes de continuar.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master</pre>

<h2><em>02</em> Mude o hello.html </h2>

<p>Acontece de você modificar o arquivo no seu diretório de trabalho local e às vezes querer descartar as mudanças que você fez commit. É aqui que o comando checkout vai te ajudar.</p>

<p>Faça mudanças ao arquivo hello.html na forma de um comentário indesejado.</p>

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

<p>Primeiro de tudo, confira o status do repositório de trabalho.</p>

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

<p>Nós vemos que o arquivo <code>hello.html</code> foi modificado, mas ainda não está no stage.</p>

<h2><em>04</em> Desfazendo as mudanças no diretório de trabalho</h2>

<p>Use o comando <code>checkout</code> para remover a versão do arquivo <code>hello.html</code> que está no repositório.</p>

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

<p>O comando status mostra que não existem mudanças que não estão no stage no repositório de trabalho. E o &#8220;comentário ruim&#8221; não está mais no arquivo.</p>
