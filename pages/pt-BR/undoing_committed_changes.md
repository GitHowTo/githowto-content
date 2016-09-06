---
view: page
title: "16. Desfazendo commits"
---

<h3>Metas</h3>

<ul><li>Aprender como desfazer commits no reposit&oacute;rio local.</li></ul>

<h2><em>01</em> Desfazendo commits</h2>

<p>Algumas vezes voc&ecirc; percebe que os novos commits est&atilde;o errados e voc&ecirc; quer desfaz&ecirc;-los. Existem v&aacute;rias maneiras de resolver esse problema, mas n&oacute;s usamos a mais segura aqui.</p>

<p>Para desfazer o commit, vamos criar um novo commit desfazendo as modifica&ccedil;&otilde;es n&atilde;o desejadas.</p>

<h2><em>02</em> Edite o arquivo e fa&ccedil;a um commit</h2>

<p>Substitua o arquivo <code>hello.html</code> com o seguinte.</p>

<h4 class="h4-pre">Arquivo: <em>hello.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
    <strong>&lt;!-- This is an unwanted but committed change --&gt;</strong>
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add hello.html
git commit -m "Oops, we didn't want this commit"</pre>

<h2><em>03</em> Fa&ccedil;a um commit com as novas modifica&ccedil;&otilde;es que desfazem as modifica&ccedil;&otilde;es anteriores</h2>

<p>Para desfazer o commit, precisamos de criar um commit que deleta as modifica&ccedil;&otilde;es feitas pelo commit indesejado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git revert HEAD</pre>

<p>V&aacute; para o editor, onde voc&ecirc; consegue editar a mensagem padr&atilde;o do commit ou deix&aacute;-la como est&aacute;. Salve e feche o arquivo.</p>

<p>Voc&ecirc; ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git revert HEAD --no-edit
[master 45fa96b] Revert "Oops, we didn't want this commit"
 1 files changed, 1 insertions(+), 1 deletions(-)</pre>

<p>J&aacute; que desfizemos o &uacute;ltimo commit, n&oacute;s podemos usar <code>HEAD</code> como o argumento para desfaz&ecirc;-lo. N&oacute;s podemos cancelar qualquer commit no hist&oacute;rico, apontando seu hash.</p>

<p class="note"><strong>Nota:</strong> O comando <code>--no-edit</code> pode ser ignorado. Ele era desnecess&aacute;rio para gerar as informa&ccedil;&otilde;es de sa&iacute;da sem abrir o editor.</p>

<h2><em>04</em> Confira o log</h2>

<p>Conferir o log mostra os cancelamentos e commits indesejados no nosso reposit&oacute;rio.</p>

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

<p>Essa t&eacute;cnica pode ser aplicada para qualquer commit (mas podem surgir conflitos). &Eacute; seguro us&aacute;-la mesmo em branches p&uacute;blicos de reposit&oacute;rios remotos.</p>

<h2><em>05</em> Pr&oacute;ximo</h2>

<p>A seguir vamos olhar a t&eacute;cnica que pode ser usada para remover o &uacute;ltimo commit do hist&oacute;rico do reposit&oacute;rio.</p>
