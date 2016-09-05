---
view: page
title: "29. Criando um conflito"
---

<h3>Metas</h3>

<ul><li>Criar um conflito de mudan&ccedil;as no branch master.</li></ul>

<h2><em>01</em> Voltar para o master e criar o conflito</h2>

<p>Volte para o branch master e fa&ccedil;a as seguintes altera&ccedil;&otilde;es:</p>

<pre class="instructions">git checkout master</pre>

<h4 class="h4-pre">Arquivo: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- no style --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World! <strong>Life is great!</strong>&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m 'Life is great!'</pre>

(<b>Aviso:</b> tenha certeza que voc&ecirc; usou aspas simples para evitar problemas com o bash e o caractere <code>!</code>)

<h2><em>02</em> Visualize os branches</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist --all
* 454ec68 2011-03-09 | Life is great! (HEAD, master) [Alexander Shvets]
| * 5813a3f 2011-03-09 | Merge branch 'master' into style (style) [Alexander Shvets]
| |\  
| |/  
|/|
* | 6c0f848 2011-03-09 | Added README [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html [Alexander Shvets]
| * 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
| * 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Depois de um commit "Added README" o branch master foi fundido com o branch style, mas existe um commit aditional do master, que n&atilde;o foi fundido com o branch style.</p>

<h2><em>03</em> Pr&oacute;ximo</h2>

<p>A &uacute;ltima modifica&ccedil;&atilde;o feita no master entra em conflito com algumas mudan&ccedil;as do style. No pr&oacute;ximo passo n&oacute;s vamos resolver esse conflito.</p>
