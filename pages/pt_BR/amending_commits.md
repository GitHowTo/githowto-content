---
view: page
title: "19. Mudando commits"
---

<h3>Metas</h3>

<ul><li>Aprender como modificar um commit j&aacute; existente</li></ul>

<h2><em>01</em> Mude a p&aacute;gina e fa&ccedil;a um commit</h2>

<p>Coloque um coment&aacute;rio de autor na p&aacute;gina.</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html
git commit -m "Add an author comment"</pre>

<h2><em>02</em> Oops... precisa do e-mail</h2>

<p>Depois de fazer o commit, voc&ecirc; percebe que todo bom coment&aacute;rio deveria incluir o e-mail do autor. Edite a p&aacute;gina hello para fornecer um e-mail.</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;</strong>
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Mude o commit anterior</h2>

<p>N&oacute;s n&atilde;o queremos criar outro commit apenas para o e-mail. Vamos mudar o commit anterior e adicionar o endere&ccedil;o de e-mail.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html
git commit --amend -m "Add an author/email comment"</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git add hello.html
$ git commit --amend -m "Add an author/email comment"
[master 6a78635] Add an author/email comment
 1 files changed, 2 insertions(+), 1 deletions(-)</pre>

<h2><em>04</em> Olhar o hist&oacute;rico</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist
* 6a78635 2011-03-09 | Add an author/email comment (HEAD, master) [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>O novo commit "author/email" substitui o commit original "author". O mesmo pode ser obtido usando o comando <code>reset</code> no branch e fazendo novamente o commit com as mudan&ccedil;as.</p>
