---
view: page
title: "3. Criando um projeto"
---

<h3>Metas</h3>

<ul><li>Aprender a criar um repositório git do início.</li></ul>

<h2><em>01</em> Crie uma página de "Hello, World"</h2>

<p>Comece com um diretório de trabalho vazio (por exemplo, Work, se você fez download do arquivo do último passo) e crie um diretório vazio chamado “hello”. Então, crie um arquivo <code>hello.html</code> dentro dele com o conteúdo indicado abaixo.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">mkdir hello
cd hello
touch hello.html</pre>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file">Hello, World</pre>

<h2><em>02</em> Crie um repositório</h2>

<p>Então você tem um diretório que tem um arquivo. Execute o comando git init para criar um repositório do git a partir desse diretório.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git init</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git init
Initialized empty Git repository in /Users/alex/Documents/Presentations/githowto/auto/hello/.git/
</pre>

<h2><em>03</em> Adicione a página ao repositório</h2>

<p>Agora vamos adicionar a página “Hello, World” ao repositório.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html
git commit -m "First Commit"</pre>

<p>Você verá &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git add hello.html
$ git commit -m "First Commit"
[master (root-commit) 911e8c9] First Commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 hello.html</pre>
