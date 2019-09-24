---
view: page
title: "17. Removendo um commit de um branch"
---

<h3>Metas</h3>

<ul><li>Aprender a deletar os commits mais recentes de um branch</li></ul>

<p><code>Revert</code> &eacute; um comando poderoso da se&ccedil;&atilde;o anterior que te permite cancelar quaisquer commits para um reposit&oacute;rio. Apesar disso, tanto os commits originais quanto os cancelados permanecem vis&iacute;veis no hist&oacute;rico do branch (quando usamos o comando <code>git log</code>).</p>

<p>Frequentemente depois que um commit &eacute; feito percebemos que ele era um erro. Seria legal ter um comando de desfazer que permitisse deletar o commit incorreto imediatamente. Esse comando preveniria a apari&ccedil;&atilde;o de um commit indesejado no hist&oacute;rico do <code>git log</code>.</p>

<h2><em>01</em> O comando <code>reset</code></h2>

<p>N&oacute;s j&aacute; usamos o comando reset para equiparar o buffer zone e o commit selecionado (commit HEAD foi usado na li&ccedil;&atilde;o anterior).</p>

<p>Quando uma refer&ecirc;ncia a um commit &eacute; dada (Exemplo: um branch, hash, ou tag name), o comando <code>reset</code> vai...</p>

<ol>
<li>Sobrescrever o branch atual para que ele aponte para o commit correto</li>
<li>Opcionalmente resetar o buffer zone para que ele satisfazer o commit especificado</li>
<li>Opcionalmente resetar o dir&eacute;torio de trabalho para que ele equipare-se ao commit especificado</li>
</ol>

<h2><em>02</em> Cheque nosso hist&oacute;rico</h2>

<p>Vamos fazer um r&aacute;pido scan do nosso hist&oacute;rico de commits.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (HEAD, master) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>N&oacute;s vemos que os dois &uacute;ltimos commits desse branch s&atilde;o "Oops" and "Revert Oops". Vamos remov&ecirc;-los com o comando reset.</p>

<h2><em>03</em> Marque esse branch primeiro</h2>

<p>Vamos marcar nosso &uacute;ltimo commit com tag, para que possamos ach&aacute;-lo ap&oacute;s remover commits.</p>
<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git tag oops</pre>

<h2><em>04</em> Resete o commit para o Oops anterior</h2>

<p>No log de hist&oacute;rico (veja acima), o commit com tag «v1» est&aacute; fazendo commit sobre um commit anterior incorreto. Vamos resetar o branch para aquele ponto. Como o branch tem uma tag, podemos usar o nome da tag no comando reset (se n&atilde;o possuir uma tag, podemos usar o valor hash).</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git reset --hard v1
git hist</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git reset --hard v1
HEAD is now at fa3c141 Added HTML header
$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Nosso branch master est&aacute; apontando para o commit v1 e "Revert Oops", e commits "Oops" n&atilde;o mais existem no branch. O par&acirc;metro  <code>--hard</code> aponta que o diret&oacute;rio de trabalho deve ser atualizado para refletir o novo head do branch.</p>
<h2><em>05</em> Nada &eacute; perdido para sempre</h2>

<p>O que acontece com os commits errados? Eles ainda est&atilde;o no reposit&oacute;rio. Na verdade, ainda podemos nos referir a eles. No in&iacute;cio da li&ccedil;&atilde;o, criamos a tag «oops» para o commit cancelado. Vamos dar uma olhada em <em>all</em> (todos) commits.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist --all
* 45fa96b 2011-03-09 | Revert "Oops, we didn't want this commit" (oops) [Alexander Shvets]
* 846b90c 2011-03-09 | Oops, we didn't want this commit [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Podemos ver que os commits errados n&atilde;o foram embora. Eles n&atilde;o est&atilde;o listados mais no branch master mas ainda permanecem no reposit&oacute;rio. Eles ainda estariam no reposit&oacute;rio caso n&atilde;o tiv&eacute;ssemos colocado uma tag neles, mas s&oacute; poder&iacute;amos referenci&aacute;-los por seus nomes hash. Commits n&atilde;o referenciados continuam no reposit&oacute;rio at&eacute; que um software coletor de lixo &eacute; acionado pelo sistema.</p>

<h2><em>06</em> Perigos de resetar</h2>

<p>Resets em branches locais geralmente s&atilde;o inofensivos. As consequ&ecirc;ncias de quaisquer "acidentes" podem ser revertidos usando um commit apropriado.</p>

<p>Apesar disso, outros usu&aacute;rios que compartilham o branch podem ficar confusos se o branch compartilhado fica armazenado em reposit&oacute;rios remotos.</p>
