---
view: page
title: "34. Rebase"
---

<h3>Metas</h3>

<ul><li>Usar o comando rebase ao invés do merge.</li></ul>

<p>Então nós voltamos no histórico até antes do primeiro merge e queremos realocar as mudanças do master para o nosso branch style.</p>

<p>Dessa vez nós vamos usar o comando rebase ao invés do merge.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout style
git rebase master
git hist</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$
$ git rebase master
First, rewinding head to replay your work on top of it...
Applying: Added css stylesheet
Applying: Hello uses style.css
Applying: Updated index.html
$
$ git hist
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, style) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README (master) [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<h2><em>01</em> Merge VS Rebase</h2>

<p>O resultado do comando rebase parece muito com o do merge. O branch style atualmente contém todas as suas mudanças, além das mudanças do branch master. A árvore de commits, porém, está um pouco diferente. A árvore de commit do branch style foi reescrita para fazer o branch master parte do histórico de commits. Isso faz com que a cadeia de commits seja mais linear e legível.</p>

<h2><em>02</em> Quando usar rebase, quando usar merge?</h2>

<p>Não use o comando rebase &#8230;</p>

<ol>
	<li>Se o branch é público e compartilhado. Reescrever tais branches vai atrapalhar o trabalho de outros colegas.</li>
	<li>Quando o histórico <em>exato</em> de commits do branch é importante (porque o comando rebase reescreve o histórico de commits).</li>
</ol>
<p>Dadas as recomendações acima, eu prefiro usar rebase para branches locais e de curto prazo e merge para branches em repositórios públicos.</p>
  </div>
