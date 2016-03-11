---
view: page
title: "26. Mudanças no branch master"
---

<h3>Metas</h3>

<ul><li>Aprender como trabalhar com vários branches com diferentes (e às vezes conflitantes) modificações.</li></ul>

<p>Enquanto você está mudando o branch style, alguém decide mudar o branch master. Ele adicionou um arquivo README.</p>

<h2><em>01</em> Atualize o arquivo README com as modificações.</h2>

<h4 class="h4-pre">Arquivo: <em>README</em></h4>

<pre class="file">This is the Hello World example from the git tutorial.</pre>

<h2><em>02</em> Faça um commit das mudanças do arquivo README no branch master.</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added README"</pre>
