---
view: page
title: "12. Usando versões anteriores"
---

<h3>Metas</h3>

<ul><li>Aprender como aplicar qualquer snapshot anterior ao diretório de trabalho.</li></ul>

<p>Voltar no histórico é bem simples. O comando checkout pode copiar qualquer snapshot do repositório para o diretório de trabalho.</p>

<h2><em>01</em> Conseguindo os hashes das versões anteriores</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist</pre>

<p class="note"><strong>Nota:</strong> Não esqueça de definir o alias <code>hist</code> no seu arquivo <code>.gitconfig</code>. Se você não lembra como fazer isso, reveja a lição sobre aliases.</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist
* fa3c141 2011-03-09 | Added HTML header (HEAD, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Confira a data do log e encontre o hash do primeiro commit. Você vai achar ele na última linha do <code>git hist</code> Use o código (os seus 7 primeiros caracteres são suficientes) no comando abaixo. Depois disso, cheque o conteúdo do arquivo hello.html.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout &lt;hash&gt;
cat hello.html</pre>

<p class="note"><strong>Nota:</strong> Vários comandos dependem dos valores de hash do repositório. Já que os meus valores de hash serão diferentes dos seus, faça as substituições apropriadas no seu hash do repositório todas as vezes que você ver <code>&lt;hash&gt;</code> ou <code>&lt;treehash&gt;</code> no comando.</p>

<p>Você verá &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout 911e8c9
Note: checking out '911e8c9'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 911e8c9... First Commit
$ cat hello.html
Hello, World</pre>

<p>O resultado do comando <code>checkout</code> esclarece completamente a situação. Versões mais antigas do git vão reclamar sobre não estarem em um branch local. Mas você não precisa de preocupar com isso agora.</p>

<p>Perceba que o conteúdo do arquivo hello.html é o conteúdo padrão.</p>

<h2><em>02</em> Voltando para a versão mais atual no branch master</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout master
cat hello.html</pre>

<p>Você verá &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout master
Previous HEAD position was 911e8c9... First Commit
Switched to branch 'master'
$ cat hello.html
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

<p>&#8216;master&#8217; é o nome do branch padrão. Ao entrar em um branch pelo seu nome, você vai para a sua versão mais atual.</p>
