---
view: page
title: "10. Hist&oacute;rico"
---

<h3>Metas</h3>

<ul><li>Aprender a visualizar o hist&oacute;rico do projeto.</li></ul>

<p>Conseguir uma lista das modifica&ccedil;&otilde;es feitas &eacute; uma fun&ccedil;&atilde;o do comando <code>git log</code>.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git log</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git log
commit fa3c1411aa09441695a9e645d4371e8d749da1dc
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added HTML header

commit 8c3228730ed03116815a5cc682e8105e7d981928
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added standard HTML page tags

commit 43628f779cb333dd30d78186499f93638107f70b
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    Added h1 tag

commit 911e8c91caeab8d30ad16d56746cbd6eef72dc4c
Author: Alexander Shvets &lt;alex@githowto.com&gt;
Date:   Wed Mar 9 10:27:54 2011 -0500

    First Commit</pre>

<p>Aqui est&aacute; uma lista de todos os quatro commits do reposit&oacute;rio, que n&oacute;s fizemos at&eacute; agora.</p>

<h2><em>01</em> Hist&oacute;rico em uma linha</h2>

<p>Voc&ecirc; controla completamente o que o <code>log</code> mostra. Eu gosto do formato de linha &uacute;nica</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git log --pretty=oneline</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git log --pretty=oneline
fa3c1411aa09441695a9e645d4371e8d749da1dc Added HTML header
8c3228730ed03116815a5cc682e8105e7d981928 Added standard HTML page tags
43628f779cb333dd30d78186499f93638107f70b Added h1 tag
911e8c91caeab8d30ad16d56746cbd6eef72dc4c First Commit</pre>

<h2><em>02</em> Controlando a exibi&ccedil;&atilde;o de entradas</h2>

<p>Existem muitas op&ccedil;&otilde;es para escolher quais entradas aparecem no log. Brinque um pouco com os par&acirc;metros a seguir:</p>

<pre class="instructions">git log --pretty=oneline --max-count=2
git log --pretty=oneline --since='5 minutes ago'
git log --pretty=oneline --until='5 minutes ago'
git log --pretty=oneline --author=&lt;your name&gt;
git log --pretty=oneline --all</pre>

<p>Detalhes s&atilde;o fornecidos nas instru&ccedil;&otilde;es do <code>git-log</code>.</p>

<h2><em>03</em> Ficando chique</h2>

<p>Isso &eacute; como eu fa&ccedil;o para rever as modifica&ccedil;&otilde;es feitas na &uacute;ltima semana. Eu adiciono <code>--author=alex</code> se eu quero ver apenas as modifica&ccedil;&otilde;es que eu fiz.</p>

<pre class="instructions">git log --all --pretty=format:"%h %cd %s (%an)" --since='7 days ago'</pre>

<h2><em>04</em> O melhor formato do log</h2>

<p>Com o tempo, eu descobri que o seguinte formato &eacute; o mais adequado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short</pre>

<p>Ele fica assim:</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Vamos olhar os detalhes:</p>

<ul><li><code>--pretty="..."</code> define o formato da sa&iacute;da</li>
	<li><code>%h</code> &eacute; o hash abreviado do commit</li>
	<li><code>%d</code> mostra decora&ccedil;&otilde;es do commit (ex.: head de branches ou tags)</li>
	<li><code>%ad</code> &eacute; a data do commit</li>
	<li><code>%s</code> &eacute; o coment&aacute;rio</li>
	<li><code>%an</code> &eacute; o nome do autor =</li>
	<li><code>--graph</code> fala para o git mostrar a &aacute;rvore de commits no formato de um gr&aacute;fico de <span class="caps">ASCII</span></li>
	<li><code>--date=short</code> mant&eacute;m o formato de data pequeno e simples</li></ul>

<p>Ent&atilde;o, toda vez que voc&ecirc; quiser ver um log, voc&ecirc; ter&aacute; que digitar muito. Felizmente, n&oacute;s aprenderemos sobre aliases na pr&oacute;xima li&ccedil;&atilde;o.</p>

<h2><em>05</em> Outras ferramentas</h2>

<p>Ambos <code>gitx</code> (para Mac) e <code>gitk</code> (para qualquer plataforma) ajudam a explorar o hist&oacute;rico.</p>
