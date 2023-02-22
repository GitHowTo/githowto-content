---
view: page
title: "35. Fundindo com o branch master"
---

<h3>Metas</h3>

<ul><li>Nós mantivemos nosso branch style atualizado em relação ao branch master (usando rebase), mas agora vamos fundir as modificações de volta no master.</li></ul>

<h2><em>01</em> Fundindo style no master</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
git merge style</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout master
Switched to branch 'master'
$
$ git merge style
Updating 6c0f848..6e6c76a
Fast-forward
 index.html       |    2 +-
 lib/style.css |    8 ++++++++
 lib/hello.html   |    6 ++++--
 3 files changed, 13 insertions(+), 3 deletions(-)
 create mode 100644 lib/style.css</pre>

<p>Já que o último commit do master é anterior ao o último commit do branch style, o git consegue fundir em modo de avanço rápido - simplesmente movendo o ponteiro do branch para frente, apontando para o mesmo commit que o branch style.</p>

<p>Conflitos não surgem no fast-forward merge.</p>

<h2><em>02</em> Confira os logs</h2>

<h4 class="h4-pre">Execute:</h4>
<pre class="instructions">git hist</pre>
<h4 class="h4-pre">Resultado:</h4>
<pre class="sample">$ git hist
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, master, style) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Agora o style e o master são idênticos.</p>
