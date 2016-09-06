---
view: page
title: "39. O que &eacute; origin?"
---

<h3>Metas</h3>

<ul><li>Aprender sobre os nomes dos reposit&oacute;rios remotos.</li></ul>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git remote</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git remote
origin</pre>

<p>N&oacute;s vemos que o reposit&oacute;rio clonado sabe o nome do reposit&oacute;rio remoto padr&atilde;o. Para acessar mais informa&ccedil;&otilde;es sobre esse tal de origin:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git remote show origin</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git remote show origin
* remote origin
  Fetch URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  Push  URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  HEAD branch (remote HEAD is ambiguous, may be one of the following):
    style
    master
  Remote branches:
    style  tracked
    master tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)</pre>

<p>N&oacute;s podemos ver que o &#8220;origin&#8221; do reposit&oacute;rio remoto &eacute; o reposit&oacute;rio <strong>hello</strong> original. Reposit&oacute;rios remotos s&atilde;o tipocamente guardados em uma m&aacute;quina separada ou em um servidor centralizado. Por&eacute;m, como podemos ver, eles tamb&eacute;m podem apontar para um reposit&oacute;rio na mesma m&aacute;quina. N&atilde;o tem nada especial sobre o nome &#8220;origin&#8221;, mas existe uma conven&ccedil;&atilde;o de us&aacute;-lo para o reposit&oacute;rio prim&aacute;rio central (se houver algum).</p>
