---
view: page
title: "15. Descartando mudanças no stage (antes do commit)"
---

<h3>Metas</h3>

<ul><li>Aprender como desfazer mudanças que já estão no stage</li></ul>

<h2><em>01</em> Edite o arquivo e adicione as mudanças ao stage</h2>

<p>Faça mudanças ao arquivo <code>hello.html</code> na forma de um comentário indesejado.</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
    <strong>&lt;!-- This is an unwanted but staged comment --&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Adicione o arquivo modificado ao stage.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html</pre>

<h2><em>02</em> Verifique o status</h2>

<p>Verifique o status da mudança indesejada.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>O status mostra que a mudança está no stage e pronta para um commit;</p>

<h2><em>03</em> Revertendo a zona de buffer</h2>

<p>Felizmente, o status informado nos mostra exatamente o que devemos fazer para cancelar mudanças no stage.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git reset HEAD hello.html</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git reset HEAD hello.html
Unstaged changes after reset:
M	hello.html</pre>

<p>O comando <code>reset</code> retorna a zona do buffer para HEAD. Isso limpa a zona do buffer das mudanças que nós acabamos de adicionar ao stage.</p>

<p>O comando <code>reset</code> (padrão) não altera o diretório de trabalho. Logo, o diretório de trabalho ainda tem os comentários indesejados. Nós podemos usar o comando checkout do tutorial anterior para remover as mudanças do repositório de trabalho.</p>

<h2><em>04</em> Mudando para a versão do commit</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout hello.html
git status</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>Nosso diretório de trabalho está limpo novamente.</p>
