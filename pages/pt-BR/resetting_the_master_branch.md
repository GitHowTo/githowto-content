---
view: page
title: "33. Reset do branch master"
---

<h3>Metas</h3>

<ul><li>Resetar o branch master para um ponto anterior ao commit conflitante.</li></ul>

<h2><em>01</em> Resetando branch master</h2>

<p> O modo interativo que adicionamos ao branch master se tornou uma mudan&ccedil;a que conflita com as mudan&ccedil;as do branch style. Vamos reverter as mudan&ccedil;as do branch master para o ponto anterior &agrave; mudan&ccedil;a conflitante. Isso nos permite demonstrar o comando rebase sem nos preocupar com conflitos.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
git hist</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist
* 454ec68 2011-03-09 | Life is great! (HEAD, master) [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>O commit "Added <span class="caps">README</span>" est&aacute; imediatamente antes do modo interativo conflitante ser adicionado. Agora precisamos resetar o branch master para o commit "Added <span class="caps">README</span>" .</p>
<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git reset --hard &lt;hash&gt;
git hist --all</pre>

<p>Examine o log. Ele deve parecer como se tiv&eacute;ssemos retrocedido o reposit&oacute;rio para um ponto no tempo anterior a qualquer merge.</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git reset --hard 6c0f848
$ git hist --all
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
