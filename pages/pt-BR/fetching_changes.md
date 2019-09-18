---
view: page
title: "42. Trazendo modifica&ccedil;&otilde;es"
---

<h3>Metas</h3>

<ul><li>Aprender como trazer modifica&ccedil;&otilde;es de um reposit&oacute;rio remoto.</li></ul>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cd ../cloned_hello
git fetch
git hist --all</pre>

<p style="color:red;"><strong><span class="caps">NOTA</span>: N&oacute;s estamos agora no reposit&oacute;rio <em>cloned_hello</em></strong></p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git fetch
From /Users/alex/Documents/Presentations/githowto/auto/hello
   6e6c76a..2faa4ea  master     -&gt; origin/master
$ git hist --all
* 2faa4ea 2011-03-09 | Changed README in original repo (origin/master, origin/HEAD) [Alexander Shvets]
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, origin/style, master) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Neste momento, o reposit&oacute;rio cont&eacute;m todos os commits do reposit&oacute;rio original. Por&eacute;m, eles n&atilde;o est&atilde;o integrados com os branchs locais do reposit&oacute;rio clonado.</p>

<p>Voc&ecirc; vai ver o commit de nome &#8220;Changed <span class="caps">README</span> in original repo&#8221; no hist&oacute;rico. Perceba que o commit inclui &#8220;origin/master&#8221; e &#8220;origin/<span class="caps">HEAD</span>&#8221;.</p>

<p>Agora vamos dar uma olhada no commit &#8220;Updated index.html&#8221;. Voc&ecirc; vai ver que o branch master local aponta para esse commit, n&atilde;o para o commit que acabamos de trazer.</p>

<p>Isso nos mostra que o comando &#8220;git fetch&#8221; vai trazer os novos commits do reposit&oacute;rio remoto, mas n&atilde;o vai fundir eles com os branches locais.</p>

<h2><em>01</em> Cheque o <span class="caps">README</span></h2>

<p>N&oacute;s podemos mostrar que o arquivo <span class="caps">README</span> clonado n&atilde;o foi modificado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cat README</pre>
<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.</pre>

<p>Nenhuma mudan&ccedil;a, como voc&ecirc; pode ver</p>
