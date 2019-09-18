---
view: page
title: "3. Criando un proyecto"
---

<h3>Metas</h3>

<ul><li>Aprender a crear un reposit&oacute;rio git desde el in&iacute;cio.</li></ul>

<h2><em>01</em> Crie una p&aacute;gina de "Hello, World"</h2>

<p>Comienze con um direct&oacute;rio de trabajo vacio (por ejemplo, Work, si usted hizo el download del archivo del &uacute;ltimo paso) y crie un direct&oacute;rio vacio llamado “hello”. Ahora crie un archivo <code>hello.html</code> dentro del direct&oacute;rio hello y ponle adentro el codigo indicado abajo.</p>

<h4 class="h4-pre">Ejecute:</h4>

<pre class="instructions">mkdir hello
cd hello
touch hello.html</pre>

<h4 class="h4-pre">Archivo: <em>hello.html</em></h4>

<pre class="file">Hello, World</pre>

<h2><em>02</em> Crie un reposit&oacute;rio</h2>

<p>Entonces usted tiene un diret&oacute;rio que tiene un archivo. Ejecute el comando git init para crear un reposit&oacute;rio git a partir de ese diret&oacute;rio.</p>

<h4 class="h4-pre">Ejecute:</h4>

<pre class="instructions">git init</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git init
Initialized empty Git repository in /Users/alex/Documents/Presentations/githowto/auto/hello/.git/
</pre>

<h2><em>03</em> Adicione la p&aacute;gina al reposit&oacute;rio</h2>

<p>Ahora vamos a agregarle una a p&aacute;gina “Hello, World” al reposit&oacute;rio.</p>

<h4 class="h4-pre">Ejecute:</h4>

<pre class="instructions">git add hello.html
git commit -m "First Commit"</pre>

<p>Usted ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git add hello.html
$ git commit -m "First Commit"
[master (root-commit) 911e8c9] First Commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 hello.html</pre>
