---
view: page
title: "38. Examine o repositório clonado"
---

<h3>Metas</h3>

<ul><li>Descobrir sobre branches em repositórios remotos.</li></ul>

<h2><em>01</em> Visualizando o repositório clonado</h2>

<p>Vamos dar uma olhada no nosso repositório clonado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cd cloned_hello
ls</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ cd cloned_hello
$ ls
README
index.html
lib</pre>

<p>Você verá uma lista de todos os arquivos no nível acima ao do repositório original (<code>README</code>, <code>index.html</code> e <code>lib</code>).</p>

<h2><em>02</em> Visualizando o histórico do repositório</h2>

<h4 class="h4-pre">Execute:</h4>
<pre class="instructions">git hist --all</pre>
<h4 class="h4-pre">Resultado:</h4>
<pre class="sample">$ git hist --all
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, origin/master, origin/style, origin/HEAD, master) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Você verá uma lista de todos os commits no novo repositório, que deveriam ser iguais aos do repositório original. A única diferença deveria ser o nome dos branches.</p>

<h2><em>03</em> Branches remotos</h2>

<p>Você verá um branch <strong>master</strong> (<strong><span class="caps">HEAD</span></strong>) no histórico. Você também verá branches com nomes estranhos (<strong>origin/master</strong>, <strong>origin/style</strong> e <strong>origin/<span class="caps">HEAD</span></strong>). Nós falaremos deles depois.</p>
