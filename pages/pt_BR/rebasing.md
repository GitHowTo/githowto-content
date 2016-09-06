---
view: page
title: "34. Rebase"
---

<h3>Metas</h3>

<ul><li>Usar o comando rebase ao inv&eacute;s do merge.</li></ul>

<p>Ent&atilde;o n&oacute;s voltamos no hist&oacute;rico at&eacute; antes do primeiro merge e queremos realocar as mudan&ccedil;as do master para o nosso branch style.</p>

<p>Dessa vez n&oacute;s vamos usar o comando rebase ao inv&eacute;s do merge.</p>

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

<p>O resultado do comando rebase parece muito com o do merge. O branch style atualmente cont&eacute;m todas as suas mudan&ccedil;as, al&eacute;m das mudan&ccedil;as do branch master. A &aacute;rvore de commits, por&eacute;m, est&aacute; um pouco diferente. A &aacute;rvore de commit do branch style foi reescrita para fazer o branch master parte do hist&oacute;rico de commits. Isso faz com que a cadeia de commits seja mais linear e leg&iacute;vel.</p>

<h2><em>02</em> Quando usar rebase, quando usar merge?</h2>

<p>N&atilde;o use o comando rebase &#8230;</p>

<ol>
	<li>Se o branch &eacute; p&uacute;blico e compartilhado. Reescrever tais branches vai atrapalhar o trabalho de outros colegas.</li>
	<li>Quando o hist&oacute;rico <em>exato</em> de commits do branch &eacute; importante (porque o comando rebase reescreve o hist&oacute;rico de commits).</li>
</ol>
<p>Dadas as recomenda&ccedil;&otilde;es acima, eu prefiro usar rebase para branches locais e de curto prazo e merge para branches em reposit&oacute;rios p&uacute;blicos.</p>
  </div>
