---
view: page
title: "9. Modificações, não arquivos"
---

<h3>Metas</h3>

<ul><li>Entender que o git trabalha com as modificações, não com os arquivos.</li></ul>

<p>A maioria dos sistemas de controle de versão trabalham com arquivos. Você adiciona o arquivo no controle de código e o sistema acompanha as mudanças a partir daquele momento..</p>

<p>O Git concentra nas mudanças de um arquivo, não no arquivo em si. Um comando <code>git add file</code> não fala para o git adicionar o arquivo no repositório, mas para perceber o atual estado do arquivo para que ele seja parte de um commit depois.</p>

<p>Nós vamos tentar investigar essa diferença nessa lição.</p>

<h2><em>01</em> Primeira mudança: Adicionando tags padrão de páginas</h2>

<p>Mude a página &#8220;Hello, World&#8221; de maneira que ela passe a ter as tags padrão <code>&lt;html&gt;</code> e <code>&lt;body&gt;</code>.</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;html&gt;
  &lt;body&gt;</strong>
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  <strong>&lt;/body&gt;
&lt;/html&gt;</strong></pre>

<h2><em>02</em> Adicione essa modificação</h2>

<p>Agora adicione essa modificação para o stage do git.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>03</em> Segunda mudança: Adicione os headers do HTML</h2>

<p>Agora adicione os headers (<code>&lt;head&gt;</code> section) na página &#8220;Hello, World&#8221;.</p>

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

<p>Você verá &#8230;</p>

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

<p>Note que o arquivo hello.html está listado duas vezes no status. A primeira mudança (a adição das tags padrão) está no stage e pronta para um commit. A segunda mudança (adição dos headers) não está no stage. Se você fizesse um commit agora, os headers não teriam sido salvos no repositório.</p>

<p>Vamos conferir.</p>

<h2><em>05</em> Commit</h2>

<p>Faça um commit das mudanças que estão no stage (as tags padrão) e então confira novamente o status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git commit -m "Added standard HTML page tags"
git status</pre>

<p>Você verá &#8230;</p>

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

<p>O comando status diz que o arquivo <code>hello.html</code> tem modificações não gravadas, mas não está mais em buffer.</p>

<h2><em>06</em> Adicionando a segunda modificação</h2>

<p>Adicione a segunda modificação ao stage, depois execute o comando <code>git status</code>.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add .
git status</pre>

<p class="note"><strong>Nota:</strong> O diretório atual (&#8216;.&#8217;) vai ser nosso arquivo a adicionar. Esse é a maneira mais conveniente de adicionar todas as mudanças dos arquivos do diretório atual e suas pastas. Mas como ele adiciona tudo, é uma boa ideia conferir o status antes de fazer um <tt>add .</tt>, para ter certeza que você não adicione nenhum arquivo que não deveria ser adicionado.</p>

<p class="note">Eu queria que você visse o truque do &#8220;add .&#8221;, mas nós vamos continuar adicionando os arquivos explicitamente no futuro, por via das dúvidas.</p>

<p>Você verá &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>A segunda modificação está no stage e pronta para um commit.</p>

<h2><em>07</em> Faça um commit da segunda mudança</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git commit -m "Added HTML header"</pre>
