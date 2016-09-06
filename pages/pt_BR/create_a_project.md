---
view: page
title: "3. Criando um projeto"
---

<h3>Metas</h3>

<ul><li>Aprender a criar um reposit&oacute;rio git do in&iacute;cio.</li></ul>

<h2><em>01</em> Crie uma p&aacute;gina de "Hello, World"</h2>

<p>Comece com um diret&oacute;rio de trabalho vazio (por exemplo, Work, se voc&ecirc; fez download do arquivo do &uacute;ltimo passo) e crie um diret&oacute;rio vazio chamado “hello”. Ent&atilde;o, crie um arquivo <code>hello.html</code> dentro dele com o conte&uacute;do indicado abaixo.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">mkdir hello
cd hello
touch hello.html</pre>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file">Hello, World</pre>

<h2><em>02</em> Crie um reposit&oacute;rio</h2>

<p>Ent&atilde;o voc&ecirc; tem um diret&oacute;rio que tem um arquivo. Execute o comando git init para criar um reposit&oacute;rio do git a partir desse diret&oacute;rio.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git init</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git init
Initialized empty Git repository in /Users/alex/Documents/Presentations/githowto/auto/hello/.git/
</pre>

<h2><em>03</em> Adicione a p&aacute;gina ao reposit&oacute;rio</h2>

<p>Agora vamos adicionar a p&aacute;gina “Hello, World” ao reposit&oacute;rio.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html
git commit -m "First Commit"</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git add hello.html
$ git commit -m "First Commit"
[master (root-commit) 911e8c9] First Commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 hello.html</pre>
