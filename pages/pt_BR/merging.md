---
view: page
title: "28. Fundindo"
---

<h3>Metas</h3>

<ul><li>Aprender como fundir dois branches diferens para restaurar as modificações para um único branch.</li></ul>

<h2><em>01</em> Fundindo em um único branch</h2>

<p>Fundir junta as modificações de dois branches em um. Vamos voltar para o branch style e fundi-lo com o master.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout style
git merge master
git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ git merge master
Merge made by recursive.
 README |    1 +
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 README
$ git hist --all
*   5813a3f 2011-03-09 | Merge branch 'master' into style (HEAD, style) [Alexander Shvets]
|\  
| * 6c0f848 2011-03-09 | Added README (master) [Alexander Shvets]
* | 07a2a46 2011-03-09 | Updated index.html [Alexander Shvets]
* | 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
* | 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Pelo merge periodico entre os branches master e style, você pode acompanhar quaisquer mudanças ou modificações ocorridas para manter a compatibilidade das mudanças de estilo na linha principal.</p>

<p>Porém, isso faz com que os gráficos de commits fiquem feios. Mais tarde vamos considerar a relocação como uma alternativa à fusão.</p>

<h2><em>02</em> Próximo</h2>

<p>Mas e se as modificações no branch master conflitarem com as modificações do style?</p>
