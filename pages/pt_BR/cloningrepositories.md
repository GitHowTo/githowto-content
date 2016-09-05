---
view: page
title: "37. Clonando reposit&oacute;rios"
---

<h3>Metas</h3>

<ul><li>Aprender a fazer c&oacute;pias dos reposit&oacute;rios.</li></ul>

<p>Se voc&ecirc; est&aacute; trabalhando em grupo, &eacute; importante que voc&ecirc; entenda os pr&oacute;ximos 12 cap&iacute;tulos, porque voc&ecirc; geralmente ter&aacute; que trabalhar com reposit&oacute;rios clonados.</p>

<h2><em>01</em> V&aacute; para o seu diret&oacute;rio de trabalho</h2>

<p>V&aacute; para o diret&oacute;rio de trabalho e clone o seu reposit&oacute;rio hello.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cd ..
pwd
ls</pre>

<p style="color:red;"><strong><span class="caps">NOTA</span>: Agora n&oacute;s estamos no diret&oacute;rio de trabalho.</strong></p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ cd ..
$ pwd
/Users/alex/Documents/Presentations/githowto/auto
$ ls
hello</pre>

<p>Neste ponto voc&ecirc; deve estar no seu diret&oacute;rio &#8220;de trabalho&#8221;. Ele deve conter um &uacute;nico reposit&oacute;rio chamado &#8220;hello&#8221;.</p>
<h2><em>02</em> Crie um clone do reposit&oacute;rio hello</h2>

<p>Vamos criar um clone do reposit&oacute;rio.</p>

<h4 class="h4-pre">Execute:</h4>
<pre class="instructions">git clone hello cloned_hello
ls</pre>
<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git clone hello cloned_hello
Cloning into cloned_hello...
done.
$ ls
cloned_hello
hello</pre>

<p>Agora devem ter dois reposit&oacute;rios no seu diret&oacute;rio de trabalho: o &#8220;hello&#8221; original e o reposit&oacute;rio clonado, chamado &#8220;cloned_hello&#8221;.</p>
