---
view: page
title: "48. Submetendo modifica&ccedil;&otilde;es"
---

<h3>Metas</h3>

<ul><li>Aprender como submeter modifica&ccedil;&otilde;es para o reposit&oacute;rio remoto</li></ul>

<p>A partir de um reposit&oacute;rio limpo, geralmente compartilhado em qualquer servidor de rede, precisamos enviar nossas modifica&ccedil;&otilde;es a outros reposit&oacute;rios.
Comece criando uma modifica&ccedil;&atilde;o para ser enviada. Edite o arquivo README e fa&ccedil;a um commit</p>

<h4 class="h4-pre"> Arquivo: <em> README </em></h4>

<pre class="file">This is the Hello World example from the git tutorial.
(Changed in the original and pushed to shared)</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added shared comment to readme"</pre>

<p>Agora envie as modifica&ccedil;&otilde;es para o reposit&oacute;rio compartilhado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git push shared master</pre>
<p><em>O reposit&oacute;rio comum</em> est&aacute; recebendo nossas modifica&ccedil;&otilde;es enviadas. (Lembre-se, n&oacute;s adicionamos ele como um reposit&oacute;rio remoto na li&ccedil;&atilde;o anterior).</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git push shared master
To ../hello.git
   2faa4ea..79f507c  master -&gt; master</pre>

<p class="note"><strong>Nota:</strong> Tivemos que explicitamente especificar o branch master para submeter as mudan&ccedil;as. Isso pode ser configurado automaticamente, mas eu sempre esque&ccedil;o o comando. Para f&aacute;cil administra&ccedil;&atilde;o de seus branches remotos mude para "Git Remote Branch".</p>
