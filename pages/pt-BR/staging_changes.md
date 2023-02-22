---
view: page
title: "6. Adicionando modificações ao stage"
---

<h3>Metas</h3>

<ul><li>Aprender a adicionar modificações ao stage para os próximos commits</li></ul>

<h2><em>01</em> Adicionando modificações</h2>

<p>Agora mande o git adicionar as modificações ao stage. Confira o status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html
git status</pre>

<p>Você verá &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git add hello.html
$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Modificações no hello.html foram adicionadas ao stage. Isso quer dizer que o git sabe da modificação, mas não é permanente no repositório. O próximo commit incluirá as modificações que estão no stage.</p>

<p>Se você decidir não fazer commit da modificação, o comando status vai te lembrar que você pode usar o comando <code>git reset</code> para remover essas mudanças do stage.</p>
