---
view: page
title: "49. Removendo modificações comuns"
---

<h3>Metas</h3>

<ul><li>Aprender como extrair modificações de um repositório comum.</li></ul>

<p>Rapidamente mude para o repositório clonado e extraia as modificações recém enviadas ao repositório comum.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cd ../cloned_hello</pre>

<p style="color:red;"><strong>Nota: Estamos agora no repositório <em>cloned_hello</em>.</strong></p>

<p>Continue com …</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git remote add shared ../hello.git
git branch --track shared master
git pull
cat README</pre>
