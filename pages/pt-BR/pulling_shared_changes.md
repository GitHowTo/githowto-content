---
view: page
title: "49. Removendo modifica&ccedil;&otilde;es comuns"
---

<h3>Metas</h3>

<ul><li>Aprender como extrair modifica&ccedil;&otilde;es de um reposit&oacute;rio comum.</li></ul>

<p>Rapidamente mude para o reposit&oacute;rio clonado e extraia as modifica&ccedil;&otilde;es rec&eacute;m enviadas ao reposit&oacute;rio comum.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cd ../cloned_hello</pre>

<p style="color:red;"><strong>Nota: Estamos agora no reposit&oacute;rio <em>cloned_hello</em>.</strong></p>

<p>Continue com …</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git remote add shared ../hello.git
git branch --track shared master
git pull shared master
cat README</pre>
