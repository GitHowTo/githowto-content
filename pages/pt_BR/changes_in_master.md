---
view: page
title: "26. Mudan&ccedil;as no branch master"
---

<h3>Metas</h3>

<ul><li>Aprender como trabalhar com v&aacute;rios branches com diferentes (e &agrave;s vezes conflitantes) modifica&ccedil;&otilde;es.</li></ul>

<p>Enquanto voc&ecirc; est&aacute; mudando o branch style, algu&eacute;m decide mudar o branch master. Ele adicionou um arquivo README.</p>

<h2><em>01</em> Atualize o arquivo README com as modifica&ccedil;&otilde;es.</h2>

<h4 class="h4-pre">Arquivo: <em>README</em></h4>

<pre class="file">This is the Hello World example from the git tutorial.</pre>

<h2><em>02</em> Fa&ccedil;a um commit das mudan&ccedil;as do arquivo README no branch master.</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added README"</pre>
