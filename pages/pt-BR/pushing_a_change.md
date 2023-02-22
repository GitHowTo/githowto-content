---
view: page
title: "48. Submetendo modificações"
---

<h3>Metas</h3>

<ul><li>Aprender como submeter modificações para o repositório remoto</li></ul>

<p>A partir de um repositório limpo, geralmente compartilhado em qualquer servidor de rede, precisamos enviar nossas modificações a outros repositórios.
Comece criando uma modificação para ser enviada. Edite o arquivo README e faça um commit</p>

<h4 class="h4-pre"> Arquivo: <em> README </em></h4>

<pre class="file">This is the Hello World example from the git tutorial.
(Changed in the original and pushed to shared)</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
git add README
git commit -m "Added shared comment to readme"</pre>

<p>Agora envie as modificações para o repositório compartilhado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git push shared master</pre>
<p><em>O repositório comum</em> está recebendo nossas modificações enviadas. (Lembre-se, nós adicionamos ele como um repositório remoto na lição anterior).</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git push shared master
To ../hello.git
   2faa4ea..79f507c  master -&gt; master</pre>

<p class="note"><strong>Nota:</strong> Tivemos que explicitamente especificar o branch master para submeter as mudanças. Isso pode ser configurado automaticamente, mas eu sempre esqueço o comando. Para fácil administração de seus branches remotos mude para "Git Remote Branch".</p>
