---
view: page
title: "43. Fundindo modificações baixadas"
---

<h3>Metas</h3>

<ul><li>Aprender como colocar as modificações baixadas no branch atual e no diretório de trabalho.</li></ul>

<h2><em>01</em> Funda as modificações baixadas no branch master local</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git merge origin/master</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git merge origin/master
Updating 6e6c76a..2faa4ea
Fast-forward
 README |    1 +
 1 files changed, 1 insertions(+), 0 deletions(-)</pre>

<h2><em>02</em> Confira o <span class="caps">README</span> novamente</h2>

<p>Agora você deve ver as modificações.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cat README</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ cat README
This is the Hello World example from the git tutorial.
(changed in original)</pre>

<p>Essas são as modificações. Apesar do comando &#8220;git fetch&#8221; não fundir as mudanças, nós podemos fundi-las manualmente pelo repositório remoto.</p>

<h2><em>03</em> Próximo</h2>
<p>Agora vamos dar uma olhada na combinação de fetch e merge em um único comando.</p>
