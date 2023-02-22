---
view: page
title: "8. Fazendo commit das modificações"
---

<h3>Metas</h3>

<ul><li>Aprender a fazer commits para o repositório</li></ul>

<h2><em>01</em> Fazendo commit das modificações</h2>

<p>Bem, chega de falar sobre stage. Vamos fazer commit das mudanças que estão no stage para o repositório.</p>

<p>Quando você usou o comando <code>git commit</code> anteriormente para fazer commit da primeira versão do <code>hello.html</code> para o repositório, você incluiu a flag <code>-m</code> que permite um comentário na linha de comando. O comando de commit permite edição interativa de comentários para o commit. Agora, vamos ver como isso funciona.</p>

<p>Se você omitir a flag <code>-m</code> da linha de comando, o git vai abrir o editor da sua escolha, a partir dessa lista (em ordem de prioridade):</p>

<ul>
<li>Variável de ambiente GIT_EDITOR </li>
<li>Definição de configuração core.editor</li>
<li>Variável de ambiente <span class="caps">VISUAL</span></li>
<li>Variável de ambiente <span class="caps">EDITOR</span></li>
</ul>

<p>Eu tenho a variável <span class="caps">EDITOR</span> configurada para o <code>emacsclient</code> (disponível para Linux and Mac).</p>

<p>Vamos fazer um commit e conferir o status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git commit</pre>

<p>Você verá o seguinte no seu editor:</p>

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

<p>Na primeira linha, escreva o comentário: &#8220;Added <span class="caps">h1 tag</span>&#8221;. Salve o arquivo e saia do editor (para fazer isso no editor padrão, pressione ESC e então escreva <code>:wq</code> e aperte Enter). Você deverá ver &#8230</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">git commit
Waiting for Emacs...
[master 569aa96] Added h1 tag
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>"Waiting for Emacs&#8230;" é obtido pelo programa <code>emacsclient</code> estar enviando o arquivo para um programa emacs em execução e esperando para ele ser fechado. O resto das informações é a mensagem padrão de commits.</p>

<h2><em>02</em> Conferindo o status</h2>

<p>No final, vamos conferir o status.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git status</pre>

<p>Você verá &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
nothing to commit (working directory clean)</pre>

<p>O diretório de trabalho está limpo, você pode continuar trabalhando.</p>
