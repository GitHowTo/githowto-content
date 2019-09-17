---
view: page
title: "13. Adicionando tags a vers&otilde;es"
---

<h3>Metas</h3>

<ul><li>Aprender como adicionar tags a commits para referenciamento futuro</li></ul>

<p>Vamos chamar a vers&atilde;o atual do nosso programa "Hello" de vers&atilde;o 1 (v1).</p>

<h2><em>01</em> Criando a tag do primeiro</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git tag v1</pre>

<p>Agora, a vers&atilde;o atual da p&aacute;gina &eacute; conhecida como <em>v1</em>.</p>

<h2><em>02</em> Tags em vers&otilde;es antigas</h2>

<p>Vamos adicionar uma tag &agrave; vers&atilde;o anterior &agrave; nossa atual vers&atilde;o com o nome v1-beta. Antes de tudo, n&oacute;s vamos precisar verificar as nossas vers&otilde;es anteriores. Ao inv&eacute;s de olhar pelo hash, n&oacute;s vamos usar a nota&ccedil;&atilde;o <code>^</code> indicando &#8220;o pai de v1&#8221;.</p>

<p class="note">Se a nota&ccedil;&atilde;o <code>v1^</code> gerar problemas, tente usar <code>v1~1</code> para referenciar a mesma vers&atilde;o. Essa nota&ccedil;&atilde;o significa &#8220;a primeira vers&atilde;o antes de v1&#8221;.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout v1^
cat hello.html</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="sample">$ git checkout v1^
Note: checking out 'v1^'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 8c32287... Added standard HTML page tags
$ cat hello.html
&lt;html&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Essa &eacute; a vers&atilde;o com as tags <code>&lt;html&gt;</code> e <code>&lt;body&gt;</code>, mas sem <code>&lt;head&gt;</code>. Vamos fazer dessa a vers&atilde;o v1-beta.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git tag v1-beta</pre>

<h2><em>03</em> Acessando atrav&eacute;s do nome da tag</h2>

<p>Agora tente executar um checkout entre as duas vers&otilde;es com tags.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout v1
git checkout v1-beta</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout v1
Previous HEAD position was 8c32287... Added standard HTML page tags
HEAD is now at fa3c141... Added HTML header
$ git checkout v1-beta
Previous HEAD position was fa3c141... Added HTML header
HEAD is now at 8c32287... Added standard HTML page tags</pre>

<h2><em>04</em> Vendo tags com o comando <code>tag</code></h2>

<p>Voc&ecirc; pode ver todas as tags usadas digitando o comando <code>git tag</code>.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git tag</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git tag
v1
v1-beta</pre>

<h2><em>05</em> Vendo tags nos logs</h2>

<p>Voc&ecirc; tamb&eacute;m pode encontrar as tags no log.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist master --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist master --all
* fa3c141 2011-03-09 | Added HTML header (v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (HEAD, v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Voc&ecirc; pode ver as tags (<code>v1</code> e <code>v1-beta</code>) listadas no log juntamente com o nome do branch (<code>master</code>). O <code>HEAD</code> mostra o commit em que voc&ecirc; est&aacute; (atualmente <code>v1-beta</code>).</p>
