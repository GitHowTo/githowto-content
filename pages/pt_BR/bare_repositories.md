---
view: page
title: "46. Reposit&oacute;rios bare"
---

<h3>Metas</h3>

<ul><li>Aprender como criar reposit&oacute;rios bare.</li></ul>

<p>Reposit&oacute;rios bare (sem o diret&oacute;rio de trabalho) s&atilde;o tipicamente usados para compartilhamento.</p>

<h2><em>01</em> Criando um reposit&oacute;rio bare</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cd ..
git clone --bare hello hello.git
ls hello.git</pre>

<p style="color:red;"><strong><span class="caps">NOTA</span>: N&oacute;s estamos agora no diret&oacute;rio de trabalho</strong></p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git clone --bare hello hello.git
Cloning into bare repository hello.git...
done.
$ ls hello.git
HEAD
config
description
hooks
info
objects
packed-refs
refs</pre>

<p>Tipicamente, reposit&oacute;rios terminados em &#8216;.git&#8217; s&atilde;o bare. Como voc&ecirc; pode ver, n&atilde;o existe nenhum diret&oacute;rio de trabalho no reposit&oacute;rio hello.git. Na verdade, ele n&atilde;o &eacute; nada mais que o diret&oacute;rio .git de um reposit&oacute;rio que n&atilde;o &eacute; bare.</p>
  </div>
