---
view: page
title: "25. Navegando em Branches"
---

<h3>Metas</h3>

<ul><li>Aprender como navegar entre branches de repositórios.</li></ul>

<p>Agora o seu projeto possui dois branches:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist --all
* 07a2a46 2011-03-09 | Updated index.html (HEAD, style) [Alexander Shvets]
* 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. (master) [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<h2><em>01</em> Trocando para o branch master</h2>

<p>Para trocar o branch atual simplesmente use o comando <code>git checkout</code>.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
cat lib/hello.html</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout master
Switched to branch 'master'
$ cat lib/hello.html
&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Agora estamos no branch master. Isso pode ser provado pelo arquivo <code>hello.html</code> que não usa os styles do <code>style.css</code>.</p>

<h2><em>02</em> Vamos retornar para o branch do style.</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout style
cat lib/hello.html</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ cat lib/hello.html
&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Agora estamos de volta a um branch <strong>style</strong> que pode ser provado pelos conteúdos de <code>lib/hello.html</code>.</p>
