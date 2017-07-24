---
view: page
title: "8. Fazendo commit das modifica&ccedil;&otilde;es"
---

<h3>Metas</h3>

<ul><li>Aprender a fazer commits para o reposit&oacute;rio</li></ul>

<h2><em>01</em> Fazendo commit das modifica&ccedil;&otilde;es</h2>

<p>Bem, chega de falar sobre stage. Vamos fazer commit das mudan&ccedil;as que est&atilde;o no stage para o reposit&oacute;rio.</p>

<p>Quando voc&ecirc; usou o comando <code>git commit</code> anteriormente para fazer commit da primeira vers&atilde;o do <code>hello.html</code> para o reposit&oacute;rio, voc&ecirc; incluiu a flag <code>-m</code> que permite um coment&aacute;rio na linha de comando. O comando de commit permite edi&ccedil;&atilde;o interativa de coment&aacute;rios para o commit. Agora, vamos ver como isso funciona.</p>

<p>Se voc&ecirc; omitir a flag <code>-m</code> da linha de comando, o git vai abrir o editor da sua escolha, a partir dessa lista (em ordem de prioridade):</p>

<ul>
<li>Vari&aacute;vel de ambiente GIT_EDITOR </li>
<li>Defini&ccedil;&atilde;o de configura&ccedil;&atilde;o core.editor</li>
<li>Vari&aacute;vel de ambiente <span class="caps">VISUAL</span></li>
<li>Vari&aacute;vel de ambiente <span class="caps">EDITOR</span></li>
</ul>

<p>Eu tenho a vari&aacute;vel <span class="caps">EDITOR</span> configurada para o <code>emacsclient</code> (dispon&iacute;vel para Linux and Mac).</p>

<p>Vamos fazer um commit e conferir o status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git commit</pre>

<p>Voc&ecirc; ver&aacute; o seguinte no seu editor:</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">|
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# On branch master
# Changes to be committed:
#   (use "git reset HEAD &lt;file&gt;..." to unstage)
#
#	modified:   hello.html
#</pre>

<p>Na primeira linha, escreva o coment&aacute;rio: &#8220;Added <span class="caps">h1 tag</span>&#8221;. Salve o arquivo e saia do editor (para fazer isso no editor padr&atilde;o, pressione ESC e ent&atilde;o escreva <code>:wq</code> e aperte Enter). Voc&ecirc; dever&aacute; ver &#8230</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">git commit
Waiting for Emacs...
[master 569aa96] Added h1 tag
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>"Waiting for Emacs&#8230;" &eacute; obtido pelo programa <code>emacsclient</code> estar enviando o arquivo para um programa emacs em execu&ccedil;&atilde;o e esperando para ele ser fechado. O resto das informa&ccedil;&otilde;es &eacute; a mensagem padr&atilde;o de commits.</p>

<h2><em>02</em> Conferindo o status</h2>

<p>No final, vamos conferir o status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>O diret&oacute;rio de trabalho est&aacute; limpo, voc&ecirc; pode continuar trabalhando.</p>
