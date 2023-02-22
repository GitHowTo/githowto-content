---
view: page
title: "27. Visualizando os diferentes branches"
---

<h3>Metas</h3>

<ul><li>Aprender como visualizar os diferentes branches no repositório.</li></ul>

<h2><em>01</em> Vendo o branch atual</h2>

<p>Agora nós temos um repositório com dois branches diferentes. Para ver branches e suas diferenças, use o comando log como se segue.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist --all
* 6c0f848 2011-03-09 | Added README (HEAD, master) [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html (style) [Alexander Shvets]
| * 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
| * 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Nós temos a oportunidade de ver o <code>--graph</code> do <code>git hist</code> em ação. Adicionando a opção <code>--graph</code> ao <code>git log</code> faz com que ele crie uma árvore de commits com a ajuda de caracteres ASCII simples. Nós vemos ambos os branches (style e master) e que o branch atual é o master HEAD. O branch index.html adicionado vai antes de ambos os branches.</p>

<p>A flag <code>--all</code> garante que nós vejamos todos os branches. Por padrão, apenas o branch atual é mostrado.</p>
