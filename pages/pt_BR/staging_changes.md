---
view: page
title: "6. Adicionando modifica&ccedil;&otilde;es ao stage"
---

<h3>Metas</h3>

<ul><li>Aprender a adicionar modifica&ccedil;&otilde;es ao stage para os pr&oacute;ximos commits</li></ul>

<h2><em>01</em> Adicionando modifica&ccedil;&otilde;es</h2>

<p>Agora mande o git adicionar as modifica&ccedil;&otilde;es ao stage. Confira o status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html
git status</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git add hello.html
$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Modifica&ccedil;&otilde;es no hello.html foram adicionadas ao stage. Isso quer dizer que o git sabe da modifica&ccedil;&atilde;o, mas n&atilde;o &eacute; permanente no reposit&oacute;rio. O pr&oacute;ximo commit incluir&aacute; as modifica&ccedil;&otilde;es que est&atilde;o no stage.</p>

<p>Se voc&ecirc; decidir n&atilde;o fazer commit da modifica&ccedil;&atilde;o, o comando status vai te lembrar que voc&ecirc; pode usar o comando <code>git reset</code> para remover essas mudan&ccedil;as do stage.</p>
