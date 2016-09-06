---
view: page
title: "27. Visualizando os diferentes branches"
---

<h3>Metas</h3>

<ul><li>Aprender como visualizar os diferentes branches no reposit&oacute;rio.</li></ul>

<h2><em>01</em> Vendo o branch atual</h2>

<p>Agora n&oacute;s temos um reposit&oacute;rio com dois branches diferentes. Para ver branches e suas diferen&ccedil;as, use o comando log como se segue.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist --all
* 6c0f848 2011-03-09 | Added README (HEAD, master) [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html (style) [Alexander Shvets]
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

<p>N&oacute;s temos a oportunidade de ver o <code>--graph</code> do <code>git hist</code> em a&ccedil;&atilde;o. Adicionando a op&ccedil;&atilde;o <code>--graph</code> ao <code>git log</code> faz com que ele crie uma &aacute;rvore de commits com a ajuda de caracteres ASCII simples. N&oacute;s vemos ambos os branches (style e master) e que o branch atual &eacute; o master HEAD. O branch index.html adicionado vai antes de ambos os branches.</p>

<p>A flag <code>--all</code> garante que n&oacute;s vejamos todos os branches. Por padr&atilde;o, apenas o branch atual &eacute; mostrado.</p>
