---
view: page
title: "43. Fundindo modifica&ccedil;&otilde;es baixadas"
---

<h3>Metas</h3>

<ul><li>Aprender como colocar as modifica&ccedil;&otilde;es baixadas no branch atual e no diret&oacute;rio de trabalho.</li></ul>

<h2><em>01</em> Funda as modifica&ccedil;&otilde;es baixadas no branch master local</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git merge origin/master</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git merge origin/master
Updating 6e6c76a..2faa4ea
Fast-forward
 README |    1 +
 1 files changed, 1 insertions(+), 0 deletions(-)</pre>

<h2><em>02</em> Confira o <span class="caps">README</span> novamente</h2>

<p>Agora voc&ecirc; deve ver as modifica&ccedil;&otilde;es.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cat README</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.
(changed in original)</pre>

<p>Essas s&atilde;o as modifica&ccedil;&otilde;es. Apesar do comando &#8220;git fetch&#8221; n&atilde;o fundir as mudan&ccedil;as, n&oacute;s podemos fundi-las manualmente pelo reposit&oacute;rio remoto.</p>

<h2><em>03</em> Pr&oacute;ximo</h2>
<p>Agora vamos dar uma olhada na combina&ccedil;&atilde;o de fetch e merge em um &uacute;nico comando.</p>
