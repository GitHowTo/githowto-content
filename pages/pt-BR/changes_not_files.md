---
view: page
title: "9. Modifica&ccedil;&otilde;es, n&atilde;o arquivos"
---

<h3>Metas</h3>

<ul><li>Entender que o git trabalha com as modifica&ccedil;&otilde;es, n&atilde;o com os arquivos.</li></ul>

<p>A maioria dos sistemas de controle de vers&atilde;o trabalham com arquivos. Voc&ecirc; adiciona o arquivo no controle de c&oacute;digo e o sistema acompanha as mudan&ccedil;as a partir daquele momento..</p>

<p>O Git se concentra nas mudan&ccedil;as de um arquivo, n&atilde;o no arquivo em si. Um comando <code>git add file</code> n&atilde;o fala para o git adicionar o arquivo no reposit&oacute;rio, mas para perceber o atual estado do arquivo para que ele seja parte de um commit depois.</p>

<p>N&oacute;s vamos tentar investigar essa diferen&ccedil;a nesta li&ccedil;&atilde;o.</p>

<h2><em>01</em> Primeira mudan&ccedil;a: Adicionando tags padr&atilde;o de p&aacute;ginas</h2>

<p>Mude a p&aacute;gina &#8220;Hello, World&#8221; de maneira que ela passe a ter as tags padr&atilde;o <code>&lt;html&gt;</code> e <code>&lt;body&gt;</code>.</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;html&gt;
  &lt;body&gt;</strong>
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  <strong>&lt;/body&gt;
&lt;/html&gt;</strong></pre>

<h2><em>02</em> Adicione essa modifica&ccedil;&atilde;o</h2>

<p>Agora adicione essa modifica&ccedil;&atilde;o para o stage do git.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>03</em> Segunda mudan&ccedil;a: Adicione os headers do HTML</h2>

<p>Agora adicione os headers (<code>&lt;head&gt;</code> section) na p&aacute;gina &#8220;Hello, World&#8221;.</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>04</em> Confira o status atual</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#</pre>

<p>Note que o arquivo hello.html est&aacute; listado duas vezes no status. A primeira mudan&ccedil;a (a adi&ccedil;&atilde;o das tags padr&atilde;o) est&aacute; no stage e pronta para um commit. A segunda mudan&ccedil;a (adi&ccedil;&atilde;o dos headers) n&atilde;o est&aacute; no stage. Se voc&ecirc; fizesse um commit agora, os headers n&atilde;o teriam sido salvos no reposit&oacute;rio.</p>

<p>Vamos conferir.</p>

<h2><em>05</em> Commit</h2>

<p>Fa&ccedil;a um commit das mudan&ccedil;as que est&atilde;o no stage (as tags padr&atilde;o) e ent&atilde;o confira novamente o status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git commit -m "Added standard HTML page tags"
git status</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git commit -m "Added standard HTML page tags"
[master 8c32287] Added standard HTML page tags
 1 files changed, 3 insertions(+), 1 deletions(-)
$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>O comando status diz que o arquivo <code>hello.html</code> tem modifica&ccedil;&otilde;es n&atilde;o gravadas, mas n&atilde;o est&aacute; mais em buffer.</p>

<h2><em>06</em> Adicionando a segunda modifica&ccedil;&atilde;o</h2>

<p>Adicione a segunda modifica&ccedil;&atilde;o ao stage, depois execute o comando <code>git status</code>.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add .
git status</pre>

<p class="note"><strong>Nota:</strong> O diret&oacute;rio atual (&#8216;.&#8217;) vai ser nosso arquivo a adicionar. Essa &eacute; a maneira mais conveniente de adicionar todas as mudan&ccedil;as dos arquivos do diret&oacute;rio atual e suas pastas. Mas como ele adiciona tudo, &eacute; uma boa ideia conferir o status antes de fazer um <tt>add .</tt>, para ter certeza que voc&ecirc; n&atilde;o adicione nenhum arquivo que n&atilde;o deveria ser adicionado.</p>

<p class="note">Eu queria que voc&ecirc; visse o truque do &#8220;add .&#8221;, mas n&oacute;s vamos continuar adicionando os arquivos explicitamente no futuro, por via das d&uacute;vidas.</p>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>A segunda modifica&ccedil;&atilde;o est&aacute; no stage e pronta para um commit.</p>

<h2><em>07</em> Fa&ccedil;a um commit da segunda mudan&ccedil;a</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git commit -m "Added HTML header"</pre>
