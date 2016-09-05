---
view: page
title: "40. Branches remotos"
---

<h3>Metas</h3>

<ul><li>Aprender sobre branches locais e remotos</li></ul>

<p>Vamos dar uma olhada nos branches do nosso reposit&oacute;rio clonado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git branch</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git branch
* master</pre>

<p>Como podemos ver, apenas o branch master est&aacute; listado. Onde est&aacute; o branch style? <code>git branch</code> lista apenas os branches locais, por padr&atilde;o.</p>
<h2><em>01</em> Lista dos branches remotos</h2>

<p>Para ver todos os branches, use o seguinte comando:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git branch -a</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git branch -a
* master
  remotes/origin/HEAD -&gt; origin/master
  remotes/origin/style
  remotes/origin/master</pre>

<p>O Git lista todos os commits do reposit&oacute;rio original, mas os branches do reposit&oacute;rio remoto n&atilde;o s&atilde;o tratados como os locais. Se n&oacute;s precisamos do nosso pr&oacute;prio branch <strong>style</strong>, teremos que cri&aacute;-lo. Em um minuto voc&ecirc; ver&aacute; como isso &eacute; feito.</p>
