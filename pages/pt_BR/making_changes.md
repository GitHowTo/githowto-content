---
view: page
title: "5. Fazendo modificações"
---

<h3>Metas</h3>

<ul><li>Aprender a monitorar o estado do dirétorio de trabalho</li></ul>

<h2><em>01</em> Modificar a página de “Hello, World”</h2>

<p>Vamos adicionar algumas tags HTML para a nossa saudação. Modifique os conteúdos do arquivo para:</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;h1&gt;</strong>Hello, World!<strong>&lt;/h1&gt;</strong></pre>

<h2><em>02</em> Conferindo o status</h2>

<p>Confira o status do diretório de trabalho.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

<p>Você verá &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>O primeiro aspecto importante aqui é que o git sabe que o arquivo <code>hello.html</code> foi modificado, mas essas modificações ainda não sofreram commit para o repositório.</p>

<p>Outro aspecto é que a mensagem de status oferece dicas sobre o que fazer em seguida. Se você quiser adicionar essas modificações para o repositório, use <code>git add</code>. Para desfazer as modificações use <code>git checkout</code>.</p>

<h2><em>03</em> Próximo...</h2>

<p>Colocando as modificações no stage.</p>
